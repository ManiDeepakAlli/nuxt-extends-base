<!-- MainComponent.vue -->
<template>
  <div class="home">
    <h1>Welcome to Our Ecommerce Store</h1>
    <div class="product-list">
      <product-card
        v-for="product in products"
        :key="product.id"
        :product="product"
        :add-to-cart="addToCart"
      />
    </div>
  </div>
</template>

<script>
import ProductCard from "@/components/ProductCard.vue";

export default {
  components: {
    ProductCard,
  },
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
</style>
