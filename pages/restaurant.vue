<template>
  <main class="content restaurant">
    <div class="restaurantheading">
      <h1>Restaurants</h1>
      <AppSelect @change="selectedRestaurant = $event" />
      <p>{{ $data }}</p>
    </div>

    <AppRestaurantInfo :datasource="filterRestaurants" />
  </main>
</template>

<script>
import AppRestaurantInfo from "@/components/AppRestaurantInfo.vue";
import AppSelect from "@/components/AppSelect.vue";
import { mapState } from "vuex";

export default {
  components: {
    AppSelect,
    AppRestaurantInfo
  },
  data: () => {
    return { selectedRestaurant: "" };
  },
  computed: {
    ...mapState(["fooddata"]),
    filterRestaurants() {
      if (this.selectedRestaurant) {
        return this.fooddata.filter(el => {
          const name = el.name.toLowerCase();
          return name.includes(this.selectedRestaurant);
        });
      }
      return this.fooddata;
    }
  }
};
</script>

<style lang="scss" scoped></style>
