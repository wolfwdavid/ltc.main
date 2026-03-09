<script>
  const products = [
    {
      image: '/img/product-small.jpg',
      alt: 'Small Vesta Holder',
      description: 'Vesta eating utensil holder (small, fits most thin silverware)',
      price: '$20.00'
    },
    {
      image: '/img/product-medium.jpg',
      alt: 'Medium Vesta Holder',
      description: 'Vesta eating utensil holder (medium, fits most silverware) (recommended)',
      price: '$20.00'
    },
    {
      image: '/img/large.png',
      alt: 'Large Vesta Holder',
      description: 'Vesta eating utensil holder (large, fits most thick silverware & plastics)',
      price: '$20.00'
    }
  ];

  function addToCart(title) {
    alert(`Added "${title}" to your cart!`);
  }
</script>

<svelte:head>
  <title>Shop - Level The Curve</title>
</svelte:head>

<section class="shop-grid">
  <h2>EZ ADAPT</h2>
  <div class="product-grid">
    {#each products as product}
      <div class="product-card">
        <img src={product.image} alt={product.alt} />
        <p>{product.description}</p>
        <span>{product.price}</span>
      </div>
    {/each}
  </div>
</section>

<style>
  .shop-grid {
    padding: 60px 20px;
    text-align: center;
  }

  .shop-grid h2 {
    font-size: 24px;
    margin-bottom: 30px;
    letter-spacing: 1px;
  }

  .product-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 40px;
  }

  .product-card {
    max-width: 300px;
    text-align: center;
  }

  .product-card img {
    width: 100%;
    max-width: 300px;
    height: auto;
    border-radius: 4px;
    object-fit: contain;
  }

  .product-card p {
    margin: 12px 0 6px;
    font-size: 15px;
    color: #333;
  }

  .product-card span {
    font-weight: bold;
    font-size: 16px;
    display: block;
    margin-top: 4px;
  }
</style>
