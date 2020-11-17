<template>
  <div class="additionaly">
    <div class="additionaly__stars">
      <img class="additionaly__star" v-if="stars >= 5" src="../assets/star.png">
      <img class="additionaly__star" v-if="stars >= 4" src="../assets/star.png">
      <img class="additionaly__star" v-if="stars >= 3" src="../assets/star.png">
      <img class="additionaly__star" v-if="stars >= 2" src="../assets/star.png">
      <img class="additionaly__star" src="../assets/star.png">
    </div>
    <p class="additionaly__stars-count">{{stars}} {{startCountMsg}}
    </p>
    <p class="additionaly__type">{{type}}</p>
  </div>
</template>

<script>

export default {
  name: 'Additionaly',
  props: ['stars', 'type'],
  data () {
    return {
      startCountMsg: this.stars === 5
        ? 'звезд'
        : 'звезды'
    }
  }
}
</script>

<style scoped>
  .additionaly {
    display: flex;
    align-items: center;
  }
  .additionaly__stars,
  .additionaly__stars-count {
    margin-right: 5px;
  }
  .additionaly__star {
    margin-right: 2px;
  }
  .additionaly__type {
    padding: 2px 5px;
    color: #515151;

    border: solid #d4d4d4 1px;
  }
</style>
