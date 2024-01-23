<template>
    <img :src="product.image" alt="Product Image" class="product-image" />
        <h2>{{ product.name }}</h2>
        <p>{{ product.description }}</p>
        <p class="price">{{ product.price }} USD</p>
    <button @click="addToCart(product)">Add to Cart</button>
</template  
