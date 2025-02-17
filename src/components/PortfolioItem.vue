<template>
  <div class="portfolio-item">
    <img :src="item.image" :alt="item.title" />
    <h3>{{ item.title }}</h3>
    <p>{{ item.description }}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "PortfolioItem",
  props: {
    item: {
      type: Object as () => {
        title: string;
        image: string;
        description: string;
      },
      required: true,
    },
  },
});
</script>

<style scoped>
.portfolio-item {
  background-color: black;
  /* Стили для элемента портфолио */
  color: antiquewhite;
}
</style>
