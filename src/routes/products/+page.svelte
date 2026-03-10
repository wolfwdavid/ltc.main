<script>
  const projects = [
    {
      title: 'UNIVERSAL EATING TOOL',
      description: 'Whatever it is, the way you tell your story online can make all the difference.',
      image: '/img/ezadapt.png',
      alt: 'Universal Eating Tool',
      link: '/products/eating-tool'
    },
    {
      title: 'LAWRENCE CHAIR',
      description: 'Whatever it is, the way you tell your story online can make all the difference.',
      image: '/img/large.png',
      alt: 'Lawrence Chair',
      link: '/products/lawrence-chair'
    },
    {
      title: 'VULCAN GRIP',
      description: 'Whatever it is, the way you tell your story online can make all the difference.',
      image: '/img/ezadapt.png',
      alt: 'Vulcan Grip',
      link: '/products/vulcan-grip'
    },
    {
      title: 'WHEELCHAIR RAMP',
      description: 'Whatever it is, the way you tell your story online can make all the difference.',
      image: '/img/large.png',
      alt: 'Wheelchair Ramp',
      link: '/products/wheelchair-ramp'
    },
    {
      title: 'LEG BAG DISPENSER',
      description: 'Whatever it is, the way you tell your story online can make all the difference.',
      image: '/img/ezadapt.png',
      alt: 'Leg Bag Dispenser',
      link: '/products/leg-bag-dispenser'
    }
  ];
</script>

<svelte:head>
  <title>Products - Level The Curve</title>
</svelte:head>

<section class="products-page">
  <h1 class="section-title">PROJECTS WE ARE WORKING ON</h1>
  <p class="subtitle">The timeline of each of our projects</p>

  <div class="projects-list">
    {#each projects as project, i}
      <div class="project-card" class:reverse={i % 2 !== 0}>
        <div class="project-image">
          <img src={project.image} alt={project.alt} />
        </div>
        <div class="project-info">
          <h2>{project.title}</h2>
          <p>{project.description}</p>
          <a href={project.link} class="learn-more">LEARN MORE</a>
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  .products-page {
    padding: 60px 40px;
    max-width: 1100px;
    margin: auto;
  }

  .subtitle {
    text-align: center;
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    color: #555;
    margin-bottom: 50px;
  }

  .projects-list {
    display: flex;
    flex-direction: column;
    gap: 50px;
  }

  .project-card {
    display: flex;
    align-items: center;
    gap: 40px;
  }

  .project-card.reverse {
    flex-direction: row-reverse;
  }

  .project-image {
    flex: 1;
    max-width: 50%;
  }

  .project-image img {
    width: 100%;
    border-radius: 4px;
    object-fit: cover;
  }

  .project-info {
    flex: 1;
    text-align: center;
  }

  .project-info h2 {
    font-family: 'Playfair Display', serif;
    font-weight: 900;
    font-size: 28px;
    text-transform: uppercase;
    letter-spacing: 2px;
    margin-bottom: 16px;
  }

  .project-info p {
    font-family: 'Inter', sans-serif;
    font-size: 14px;
    color: #555;
    line-height: 1.6;
    margin-bottom: 24px;
    font-style: italic;
  }

  .learn-more {
    display: inline-block;
    padding: 12px 28px;
    background-color: #000;
    color: #fff;
    text-decoration: none;
    font-family: 'Inter', sans-serif;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 1.5px;
    border-radius: 2px;
    transition: background-color 0.3s ease;
  }

  .learn-more:hover {
    background-color: #333;
  }

  @media (max-width: 768px) {
    .project-card,
    .project-card.reverse {
      flex-direction: column;
    }

    .project-image {
      max-width: 100%;
    }
  }
</style>
