<template>
  <div class="home">
    <ul>
      <li v-for="(product, i) in products" :key="i">
        <router-link :to="'/products/' + product.id">{{
          product.name
        }}</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      products: [
        { id: 1, name: "product 1" },
        { id: 2, name: "product 2" },
        { id: 3, name: "product 3" },
      ],
    };
  },
};
</script>
