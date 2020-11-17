<template>
  <div class="content">
    <Filters
      @change="search"
    />
    <Items v-bind:items="copiedItems"/>
  </div>
</template>

<script>
import Filters from './Filters'
import Items from './Items'

export default {
  name: 'Content',
  props: ['items'],
  data () {
    const copiedItems = this.items
    const activeFilters = []
    return {
      copiedItems,
      activeFilters
    }
  },
  components: {
    Filters,
    Items
  },
  methods: {
    search (query, types, stars) {
      this.copiedItems = this.items.filter((item) => (
        item.location.toLowerCase().includes(query.toLowerCase()) &&
        stars.some(star => +star === item.stars) &&
        types.some(type => type === item.type)
      ))
    }
  }
}
</script>

<style scoped>
.content {
  display: flex;
};
</style>
