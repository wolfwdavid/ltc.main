<script>
  import { onMount, onDestroy } from 'svelte';

  let { modelUrl = '', backgroundColor = '#f0f0f0' } = $props();

  let container;
  let renderer, scene, camera, animationId, mesh;
  let isLoading = $state(true);
  let loadError = $state('');

  let isDragging = false;
  let previousMouse = { x: 0, y: 0 };
  let initialRotation = { x: -Math.PI / 2, y: 0 };

  onMount(async () => {
    const THREE = await import('three');
    const { STLLoader } = await import('three/addons/loaders/STLLoader.js');

    const width = container.clientWidth;
    const height = container.clientHeight;

    scene = new THREE.Scene();
    scene.background = new THREE.Color(backgroundColor);

    camera = new THREE.PerspectiveCamera(45, width / height, 0.1, 1000);
    camera.position.set(0, 0, 20);

    renderer = new THREE.WebGLRenderer({ antialias: true });
    renderer.setSize(width, height);
    renderer.setPixelRatio(window.devicePixelRatio);
    renderer.toneMapping = THREE.ACESFilmicToneMapping;
    renderer.toneMappingExposure = 1.2;
    container.appendChild(renderer.domElement);

    const ambientLight = new THREE.AmbientLight(0xffffff, 0.6);
    scene.add(ambientLight);

    const dirLight1 = new THREE.DirectionalLight(0xffffff, 1.0);
    dirLight1.position.set(5, 5, 5);
    scene.add(dirLight1);

    const dirLight2 = new THREE.DirectionalLight(0xffffff, 0.5);
    dirLight2.position.set(-5, 3, -5);
    scene.add(dirLight2);

    const dirLight3 = new THREE.DirectionalLight(0xffffff, 0.3);
    dirLight3.position.set(0, -3, 0);
    scene.add(dirLight3);

    // Load STL model
    const loader = new STLLoader();
    loader.load(
      modelUrl,
      (geometry) => {
        geometry.computeVertexNormals();

        const material = new THREE.MeshPhysicalMaterial({
          color: 0xb0b0b0,
          metalness: 0.4,
          roughness: 0.4,
          clearcoat: 0.3,
        });

        mesh = new THREE.Mesh(geometry, material);

        // Center the geometry
        geometry.computeBoundingBox();
        const boundingBox = geometry.boundingBox;
        const center = new THREE.Vector3();
        boundingBox.getCenter(center);
        geometry.translate(-center.x, -center.y, -center.z);

        const size = new THREE.Vector3();
        boundingBox.getSize(size);
        const maxDim = Math.max(size.x, size.y, size.z);
        const scale = 30 / maxDim;
        mesh.scale.set(scale, scale, scale);

        // Stand upright
        mesh.rotation.x = initialRotation.x;
        mesh.rotation.y = initialRotation.y;

        scene.add(mesh);
        isLoading = false;
      },
      undefined,
      (error) => {
        console.error('Error loading STL:', error);
        loadError = 'Failed to load 3D model';
        isLoading = false;
      }
    );

    function animate() {
      animationId = requestAnimationFrame(animate);
      renderer.render(scene, camera);
    }
    animate();

    // Drag to rotate model
    const canvas = renderer.domElement;
    canvas.addEventListener('pointerdown', onPointerDown);
    canvas.addEventListener('pointermove', onPointerMove);
    canvas.addEventListener('pointerup', onPointerUp);
    canvas.addEventListener('pointerleave', onPointerUp);
    canvas.addEventListener('wheel', onWheel, { passive: false });

    window.addEventListener('resize', onResize);
  });

  function onPointerDown(e) {
    isDragging = true;
    previousMouse = { x: e.clientX, y: e.clientY };
  }

  function onPointerMove(e) {
    if (!isDragging || !mesh) return;
    const dx = e.clientX - previousMouse.x;
    const dy = e.clientY - previousMouse.y;

    mesh.rotation.y += dx * 0.01;
    mesh.rotation.x += dy * 0.01;

    previousMouse = { x: e.clientX, y: e.clientY };
  }

  function onPointerUp() {
    isDragging = false;
  }

  function onWheel(e) {
    if (!camera) return;
    e.preventDefault();
    camera.position.z += e.deltaY * 0.01;
    camera.position.z = Math.max(2, Math.min(30, camera.position.z));
  }

  onDestroy(() => {
    if (typeof window === 'undefined') return;
    if (animationId) cancelAnimationFrame(animationId);
    if (renderer) renderer.dispose();
    window.removeEventListener('resize', onResize);
  });

  function onResize() {
    if (!container || !renderer || !camera) return;
    const width = container.clientWidth;
    const height = container.clientHeight;
    camera.aspect = width / height;
    camera.updateProjectionMatrix();
    renderer.setSize(width, height);
  }

  function resetView() {
    if (!camera || !mesh) return;
    camera.position.set(0, 0, 20);
    mesh.rotation.x = initialRotation.x;
    mesh.rotation.y = initialRotation.y;
  }
</script>

<div class="viewer-wrapper">
  <div class="viewer-container" bind:this={container}>
    {#if isLoading}
      <div class="loading-overlay">
        <div class="spinner"></div>
        <p>Loading 3D Model...</p>
      </div>
    {/if}
    {#if loadError}
      <div class="loading-overlay">
        <p>{loadError}</p>
      </div>
    {/if}
  </div>
  <div class="viewer-controls">
    <span class="hint"><i class="fa fa-hand-pointer-o"></i> Drag to rotate model &bull; Scroll to zoom</span>
    <button class="reset-btn" onclick={resetView}>
      <i class="fa fa-refresh"></i> Reset View
    </button>
  </div>
</div>

<style>
  .viewer-wrapper {
    margin: 30px auto;
    max-width: 800px;
  }

  .viewer-container {
    width: 100%;
    height: 500px;
    border-radius: 8px;
    overflow: hidden;
    position: relative;
    background-color: #f0f0f0;
    cursor: grab;
  }

  .viewer-container:active {
    cursor: grabbing;
  }

  .loading-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: #333;
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    gap: 16px;
    z-index: 10;
  }

  .spinner {
    width: 36px;
    height: 36px;
    border: 3px solid rgba(0, 0, 0, 0.1);
    border-top-color: #F5D547;
    border-radius: 50%;
    animation: spin 0.8s linear infinite;
  }

  @keyframes spin {
    to { transform: rotate(360deg); }
  }

  .viewer-controls {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 12px;
    flex-wrap: wrap;
    gap: 10px;
  }

  .hint {
    font-family: 'Inter', sans-serif;
    font-size: 12px;
    color: #777;
  }

  .reset-btn {
    padding: 8px 16px;
    background-color: #000;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-family: 'Inter', sans-serif;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.5px;
    transition: background-color 0.3s ease;
  }

  .reset-btn:hover {
    background-color: #333;
  }
</style>
