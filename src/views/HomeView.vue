<template>
  <div>
    <h1>Мое Портфолио</h1>
    <div class="portfolio">
      <PortfolioItem
        v-for="item in portfolioItems"
        :key="item.title"
        :item="item"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PortfolioItem from "../components/PortfolioItem.vue";

export default defineComponent({
  name: "HomePage",
  components: {
    PortfolioItem,
  },
  setup() {
    const portfolioItems = [
      {
        title: "Работа 1",
        image: "link_to_image_1.jpg",
        description: "Описание работы 1",
      },
      {
        title: "Работа 2",
        image: "link_to_image_2.jpg",
        description: "Описание работы 2",
      },
      // Добавь больше работ
    ];

    return { portfolioItems };
  },
});
</script>

<style scoped>
.portfolio {
  background-color: black;
  /* Стили */
  color: antiquewhite;
}
</style>
