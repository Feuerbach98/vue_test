<template>
  <Content v-bind:items="itemsFromServer"/>
</template>

<script>
import Content from './components/Content'

export default {
  name: 'App',
  components: {
    Content
  },
  data () {
    return {
      itemsFromServer: [
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 4,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 4,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 2,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 5,
          type: 'Апартаменты',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 4,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 4,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 4,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 4,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 2,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 5,
          type: 'Апартаменты',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 4,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        },
        {
          id: 1,
          title: 'Mondrian Suites Berlin am Checkpoint Charlie Suites Berlin am',
          stars: 4,
          type: 'Отель',
          description: 'Этот стильный отель находится между стадионом «Мерседес-Бенц Арена» и Истсайдской галереей — самой известной...',
          location: 'Фалираки, Родос, Греция',
          price: 32566,
          imgUrl: 'https://cf.bstatic.com/xdata/images/hotel/max1024x768/52631930.webp?k=93a1a53cee05f3beb8c356e3d5757641e1d84146288be3a48b3abe058c0a8403&o=',
          rating: {
            appraisal: 4.5,
            textRating: 'Хорошо'
          },
          feedbacks: [
            'Отличное расположение Полностью новый: только что открылся в септе, поэтому все идеально: комната довольно большая и хорошо оформленная Удивительная терраса и невероятное патио с бассейном. Хороший зал с баром ...'
          ]
        }
      ]
    }
  }
}
</script>

<style>
body,
p,
h3 {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 14px;
  padding: 0 20px;
  /* margin-top: 60px; */
}
</style>
