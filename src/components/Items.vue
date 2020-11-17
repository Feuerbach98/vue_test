<template>
  <transition name="fade">
    <div class="items" v-if="items.length">
    <div >
      <Item
        v-for="item of copiedItems"
        v-bind:key="item.id"
        v-bind:item="item"
      />
    </div>
    <button class="show-more" type="button" v-on:click="addItems">Показать еще</button>
  </div>
  <div class="empty" v-else>
    <p>Записей не найдено</p>
  </div>
  </transition>
</template>

<script>
import Item from './Item'

export default {
  name: 'Items',
  props: ['items'],
  components: {
    Item
  },
  data () {
    const showingItems = 6
    const copiedItems = this.items.slice(0, showingItems)

    return {
      copiedItems,
      showingItems
    }
  },
  methods: {
    addItems () {
      const end = this.showingItems + 3 > this.items.length
        ? this.items.length
        : this.showingItems + 3

      this.copiedItems.push(...this.items.slice(this.showingItems, end))
      this.showingItems = end
    }
  }
}
</script>

<style scoped>
  .items {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .empty {
    margin: 20px;
    font-size: 2em;
    color: grey;
  }
  .show-more {
    width: 150px;
    height: 30px;
    margin: 50px;
    border: 1px solid grey;
    outline: 0;

    transition: box-shadow 0.2s;
  }
  .show-more:hover {
    cursor: pointer;
    box-shadow: 0 0 10px 1px grey;
  }
</style>
