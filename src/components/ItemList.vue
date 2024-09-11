<template>
  <div>
    <h1>Prelim</h1>
    <div v-for="(item, index) in filteredItems" :key="index">
      <Item :item="item" @add-to-cart="handleAddToCart" />
    </div>
  </div>
</template>

<script>
import Item from './Item.vue'

export default {
  name: 'ItemList',
  components: {
    Item
  },
  props: {
    items: {
      type: Array,
      required: true
    }
  },
  computed: {
    filteredItems() {
      return this.items.filter((item) => item.isVisible)
    }
  },
  methods: {
    handleAddToCart(item) {
      console.log(`Added to cart: ${item.name} - ₱${item.price}`)
    }
  }
}

