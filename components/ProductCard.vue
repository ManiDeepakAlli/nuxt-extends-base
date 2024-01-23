<!-- ProductCard.vue -->
<template>
  <div class="product">
    <img :src="product.image" :alt="product.name + ' Image'" class="product-image" />
    <h2>{{ product.name }}</h2>
    <p>{{ product.description }}</p>
    <p class="price">{{ product.price }} USD</p>
    <button @click="addToCart(product)">Add to Cart</button>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      required: true,
    },
    addToCart: {
      type: Function,
      required: true,
    },
  },
};
</script>

<style scoped>
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
