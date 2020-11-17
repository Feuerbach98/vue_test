<template>
  <div class="item">
    <div class="item__main">
      <img class="item__image" :src="item.imgUrl">
      <div class="item__content">
        <p class="item__location">
          {{item.location}}
        </p>
        <h3 class="item__title">{{item.title}}</h3>
        <div class="item__additionaly">
          <Additionaly
            v-bind:stars="item.stars"
            v-bind:type="item.type"
          />
        </div>
        <p class="item__description">{{item.description}}</p>
      </div>
    </div>
    <div class="item__feedbacks">
      <Feedbacks
        v-bind:feedbacks="item.feedbacks"
        v-bind:rating="item.rating"
      />
    </div>
    <div class="item__buy">
      <p class="item__price">от {{item.price.toLocaleString()}} ₽</p>
      <button type="button" class="item__buy-button">Забронировать</button>
    </div>
  </div>
</template>

<script>
import Additionaly from './Additionaly'
import Feedbacks from './Feedbacks'

export default {
  name: 'Item',
  props: ['item'],
  components: {
    Additionaly,
    Feedbacks
  }
}
</script>

<style scoped>
  .item {
    display: flex;
    position: relative;
    margin: 10px;
  }
  .item__main {
    display: flex;
  }
  .item__image {
    margin: 0 10px;

    width: 280px;
    height: 290px;
    object-fit: cover;
  }
  .item__location {
    font-size: 13px;
    color: #515151;
    margin-bottom: 10px;
  }
  .item__title {
    margin-bottom: 10px;
    font-size: 24px;
  }
  .item__additionaly {
    margin-bottom: 20px;
  }
  .item__description {
    width: 90%;
  }
  .item__feedbacks {
    margin: 28px 0 0 10px;
    width: 30%;
  }
  .item__buy {
    position: absolute;
    bottom: 0;
    right: 0;

    display: flex;
    align-items: center;
  }
  .item__price {
    margin-right: 10px;
    font-size: 17px;
    font-weight: bold;
  }
  .item__buy-button {
    width: 140px;
    height: 50px;

    color: white;

    border: none;
    border-radius: 2px;

    background: #FF4641;
    transition: background-color 1s;
  }
  .item__buy-button:hover {
    cursor: pointer;
    background: #f57b76;
  }
</style>
