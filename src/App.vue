<template>
  <div id="app">
    <ItemList :items="products" />
  </div>
</template>

<script>
import ItemList from './components/ItemList.vue'

export default {
  name: 'App',
  components: {
    ItemList
  },
  data() {
    return {
      products: [
        { name: 'Lenovo', price: 150, isVisible: true },
        { name: 'VivoS1 Pro', price: 200, isVisible: true },
        { name: 'Items Shoes', price: 300, isVisible: true }
      ]
    }
  }
}
</script>
