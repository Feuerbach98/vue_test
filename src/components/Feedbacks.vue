<template>
  <div v-if="feedbacks.length" class="feedbacks">
    <div class="feedbacks__top">
      <div class="feedbacks__rating">
        <img alt="" src="../assets/red-star.png">
        {{rating.appraisal}}
      </div>
      <div class="feedbacks__mark">·</div>
      <p class="feedbacks__text-rating">{{rating.textRating}}</p>
      <div class="feedbacks__mark">·</div>
      <p class="feedbacks__count">
        {{feedbacks.length}} {{feedbacks.length === 1 ? 'отзыв' : 'отзывов'}}
      </p>
    </div>
    <p class="feedbacks__last">
      {{feedbacks[0]}}
    </p>
  </div>
  <div v-else>Нет оценок.</div>
</template>

<script>
export default {
  name: 'Feedbacks',
  props: ['feedbacks', 'rating']
}
</script>

<style scoped>
  .feedbacks__top {
    display: flex;

    font-weight: bold;
  }
  .feedbacks__mark {
    color: grey;
    margin: 0 5px;
  }
  .feedbacks__last {
    margin-top: 15px;
  }
</style>
