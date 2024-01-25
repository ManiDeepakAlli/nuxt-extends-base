<!-- MainComponent.vue -->
<template>
  <div>  
    <header-component title="Ecommerce Store" />
    <div class="home">
      <h2>Welcome to Our Ecommerce Store</h2>
      <div class="product-list">
        <product-card
          v-for="product in products"
          :key="product.id"
          :product="product"
          :add-to-cart="addToCart"
        />
         <ai-suggest-component />
      </div>
    </div>
    <footer-component />
  </div>
</template>

<script>
import ProductCard from "@/components/ProductCard.vue";
import HeaderComponent from '@/components/HeaderComponent.vue';
import FooterComponent from '@/components/FooterComponent.vue';

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
          image: 'https://fakestoreapi.com/img/71-3HjGNDUL._AC_SY879._SX._UX._SY._UY_.jpg',
        },
        {
          id: 2,
          name: 'Product 2',
          description: 'Description for Product 2',
          price: 29.99,
          image: 'https://fakestoreapi.com/img/71z3kpMAYsL._AC_UY879_.jpg',
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
