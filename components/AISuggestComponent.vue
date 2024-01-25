<!-- AISuggestComponent.vue -->
<template>
  <div class="ai-suggest">
    <h3>Suggested Recommendations</h3>
    <ul>
      <li v-for="suggestion in suggestions" :key="suggestion.id">
        {{ suggestion.text }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      suggestions: [
        { id: 1, text: "Try our new arrivals for the latest trends." },
        { id: 2, text: "Customers who bought this also liked these products." },
        { id: 3, text: "Explore related categories for more options." },
        // Add more suggestions as needed
      ],
    };
  },
};
</script>

<style scoped>
.ai-suggest {
  border: 1px solid #ddd;
  border-radius: 8px;
  padding: 15px;
  margin: 20px 0;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin: 10px 0;
  color: #555;
}
</style>
