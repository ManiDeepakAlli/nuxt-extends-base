<template>
  <div class="home">
    <h1>Welcome to Our Ecommerce Store</h1>
    <div class="product-list">
      <div v-for="product in products" :key="product.id" class="product">
        <img :src="product.image" alt="Product Image" class="product-image" />
        <h2>{{ product.name }}</h2>
        <p>{{ product.description }}</p>
        <p class="price">{{ product.price }} USD</p>
        <button @click="addToCart(product)">Add to Cart</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          id: 1,
          name: 'Product 1',
          description: 'Description for Product 1',
          price: 19.99,
          image: 'path/to/product1-image.jpg',
        },
        {
          id: 2,
          name: 'Product 2',
          description: 'Description for Product 2',
          price: 29.99,
          image: 'path/to/product2-image.jpg',
        },
        // Add more products as needed
      ],
    };
  },
  methods: {
    addToCart(product) {
      // Implement your logic to add the product to the cart
      console.log(`Added ${product.name} to the cart`);
    },
  },
};
</script>

<style scoped>
.home {
  text-align: center;
  padding: 20px;
}

.product-list {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.product {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
  max-width: 200px;
}

.product-image {
  max-width: 100%;
  height: auto;
}

.price {
  font-weight: bold;
  color: green;
}
</style>
