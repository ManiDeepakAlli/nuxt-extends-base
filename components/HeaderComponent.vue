<!-- HeaderComponent.vue -->
<template>
  <header class="header">
    <h1>{{ title }}</h1>
  </header>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.header {
  background-color: #333;
  color: white;
  padding: 10px;
  text-align: center;
}
</style>
