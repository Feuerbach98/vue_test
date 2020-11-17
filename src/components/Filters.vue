<template>
  <div class="filters">
  <div class="filter">
    <div class="filter__top" v-on:click="hiddenFilters.isSearchHidden = !hiddenFilters.isSearchHidden">
      <p class="filter__title">Поиск по странам и городам:</p>
      <div
        class="filter__arrow"
        v-bind:class="{ 'filter__arrow--rotated': hiddenFilters.isSearchHidden }"
      >^</div>
    </div>
    <div
      class="filter__body"
      v-bind:class="{ 'filter__body--hidden': hiddenFilters.isSearchHidden }">
      <input
        class="filter__search"
        type="text"
        v-on:input="onSearch"
        v-model="query"
        placeholder="Например: Москва"
      >
    </div>
  </div>
  <div class="filter">
    <div class="filter__top" v-on:click="hiddenFilters.isStarsHidden = !hiddenFilters.isStarsHidden">
      <p class="filter__title">Звезды:</p>
      <div
        class="filter__arrow"
        v-bind:class="{ 'filter__arrow--rotated': hiddenFilters.isStarsHidden }"
      >^</div>
    </div>
    <div
      class="filter__body"
      v-bind:class="{ 'filter__body--hidden': hiddenFilters.isStarsHidden }"
    >
      <div>
      <input
        type="checkbox"
        id="withoutstars"
        value="0"
        v-on:change="onSearch"
        class="filter-checkbox"
        v-model="checkedStars">
      <label class="filter__checkbox-label" for="withoutstars">Без звезд</label>
      <input
        type="checkbox"
        id="1star"
        value="1"
        v-on:change="onSearch"
        class="filter-checkbox"
        v-model="checkedStars">
      <label class="filter__checkbox-label" for="1star">1 звезда</label>
      <input
        type="checkbox"
        id="2star"
        value="2"
        v-on:change="onSearch"
        class="filter-checkbox"
        v-model="checkedStars">
      <label class="filter__checkbox-label" for="2star">2 звезды</label>
      <input
        type="checkbox"
        id="3star"
        value="3"
        v-on:change="onSearch"
        class="filter-checkbox"
        v-model="checkedStars">
      <label class="filter__checkbox-label" for="3star">3 звезды</label>
      <input
        type="checkbox"
        id="4star"
        value="4"
        v-on:change="onSearch"
        class="filter-checkbox"
        v-model="checkedStars">
      <label class="filter__checkbox-label" for="4star">4 звезды</label>
      <input
        type="checkbox"
        id="5star"
        value="5"
        v-on:change="onSearch"
        class="filter-checkbox"
        v-model="checkedStars">
      <label class="filter__checkbox-label" for="5star">5 звезд</label>
    </div>
    </div>
    <div>
      <div class="filter__top" v-on:click="hiddenFilters.isTypeHidden = !hiddenFilters.isTypeHidden">
        <p class="filter__title">Тип:</p>
        <div
          class="filter__arrow"
          v-bind:class="{ 'filter__arrow--rotated': hiddenFilters.isTypeHidden }"
        >^
        </div>
      </div>
      <div
        class="filter__body"
        v-bind:class="{ 'filter__body--hidden': hiddenFilters.isTypeHidden }"
      >
      <input
        type="checkbox"
        id="hotel"
        value="Отель"
        v-on:change="onSearch"
        v-model="checkedTypes"
        class="filter__checkbox-type">
      <label class="filter__checkbox-type-label" for="hotel">Отель</label>
      <input
        type="checkbox"
        id="apartments"
        value="Апартаменты"
        v-on:change="onSearch"
        v-model="checkedTypes"
        class="filter__checkbox-type">
      <label class="filter__checkbox-type-label" for="apartments">Апартаменты</label>
      </div>
    </div>
  </div>
  <div class="filter">
    <div class="filter__top" v-on:click="hiddenFilters.isPriceHidden = !hiddenFilters.isPriceHidden">
      <p class="filter__title">Цена:</p>
      <div
        class="filter__arrow"
        v-bind:class="{ 'filter__arrow--rotated': hiddenFilters.isPriceHidden }"
      >^
      </div>
    </div>
    <div
      class="filter__body"
      v-bind:class="{ 'filter__body--hidden': hiddenFilters.isPriceHidden }"
    >
    </div>
  </div>
  </div>

</template>

<script>

export default {
  components: {
  },
  data () {
    return {
      query: '',
      checkedStars: [],
      checkedTypes: [],
      hiddenFilters: {
        isSearchHidden: false,
        isStarsHidden: false,
        isTypeHidden: false,
        isPriceHidden: false
      },
      priceMin: 0,
      priceMax: 40000
    }
  },
  methods: {
    onSearch () {
      const newQuery = this.query
      let types = this.checkedTypes
      let stars = this.checkedStars

      if (!stars.length) {
        stars = [0, 1, 2, 3, 4, 5]
      }

      if (!types.length) {
        types = ['Апартаменты', 'Отель']
      }

      this.$emit(
        'change',
        newQuery,
        types,
        stars
      )
    },
    toggleClass (prop) {
      prop = !prop
    },
    onPriceChange (values) {
      this.priceMin = values[0]
      this.priceMax = values[1]
    }
  }
}
</script>

<style scoped>
  .filters {
    display: block;
    padding-top: 10px;
    width: 250px;
    min-width: 250px;
  }
  .filter {
    margin-bottom: 20px;
  }
  .filter__top {
    display: flex;
    justify-content: space-between;
    margin: 30px 0;
  }
  .filter__title,
  .filter__arrow {
    font-weight: bold;
  }
  .filter__arrow {
    transition: 0.2s
  }
  .filter__arrow--rotated {
    transform: rotate(180deg);
  }
  .filter__top:hover {
    cursor: pointer;
  }
  .filter__body--hidden {
    display: none;
  }
  .filter__search {
    padding: 10px;
    width: 230px;
    outline: 0;
    border: 0;
    box-shadow: 0 0 10px 1px grey;

    transition: box-shadow 0.2s;
  }
  .filter__search:hover,
  .filter__search:focus {
    box-shadow: 0 0 10px 3px grey;
  }
  .filter-checkbox {
    position: absolute;
    z-index: -1;
    opacity: 0;
  }
  .filter__checkbox-label {
    display: block;
    margin-bottom: 5px;
  }
  .filter-checkbox+label {
    align-items: center;
    user-select: none;
  }
  .filter-checkbox+label::before {
    content: '';
    position: relative;
    top: 3px;

    display: inline-block;
    width: 1.1em;
    height: 1.1em;

    border: 1px solid #adb5bd;
    border-radius: 2px;
    margin-right: 0.5em;

    background-repeat: no-repeat;
    background-position: center center;
    background-size: 50% 50%;
  }
  .filter-checkbox:checked+label::before {
    border-color: #FF4641;
    background-color: #FF4641;
    background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 8 8'%3e%3cpath fill='%23fff' d='M6.564.75l-3.59 3.612-1.538-1.55L0 4.26 2.974 7.25 8 2.193z'/%3e%3c/svg%3e");
  }
  .filter__checkbox-type {
    position: absolute;
    z-index: -1;
    opacity: 0;
  }
  .filter__checkbox-type-label {
    padding: 10px;
    margin-right: 10px;
    height: 30px;
    border-radius: 15px;
    user-select: none;
  }
  .filter__checkbox-type-label:hover {
    cursor: pointer;
  }
  .filter__checkbox-type:checked+label {
    background: #FDE283;
;
}
</style>
