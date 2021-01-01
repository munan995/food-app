<template>
  <section class="restaurantinfo">
    <div v-for="store in datasource" :key="store.rating">
      <h2>
        {{ store.name }}
      </h2>
      <p>delivery Time: {{ store.deliveryTime }}</p>
      <p>
        {{ store.rating }}
      </p>
      <p v-if="store.freeDelivery" class="label">
        <span>Free delivery!</span>
      </p>
      <div class="row">
        <div
          v-for="menuitem in store.menu"
          :key="menuitem.id"
          :style="`background: url(/${menuitem.img}) no-repeat center center`"
          class="items"
        >
          <div class="iteminfo">
            <div>
              <h4>{{ menuitem.item }}</h4>
              <p>{{ priceFormatting(menuitem.price) }}</p>
            </div>
            <nuxt-link :to="`/items/${menuitem.id}`">
              <button class="ghost">View item</button>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    datasource: {
      type: [Array, Object]
    }
  },
  methods: {
    priceFormatting: (price = 200) => `$ ${price.toFixed(2)}`
  }
};
</script>

<style lang="scss" scoped></style>
