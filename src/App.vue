<template>
  <div class="container">

    <filter-block :isShort="isShort">

    </filter-block>

    <offer-block v-for="block in blocks" :key="block.id" :name="block.name" :offers="block.offers">

    </offer-block>

  </div>
</template>

<script>
import FilterBlock from '@/components/FilterBlock/filter-block.vue';
import OfferBlock from '@/components/OfferBlock/offer-block.vue';
import '@/assets/style.scss';

export default {

  components: {
    OfferBlock,
    FilterBlock
  },

  created() {

    this.positionY = window.scrollY;
    window.addEventListener('scroll', this.toggleSeacrh);

  },

  unmounted() {

    window.removeEventListener('scroll', this.toggleSeacrh);

  },

  data() {
    return {
      isShort: false,
      positionY: null,
      blocks: [
        {
          id: 1,
          name: 'Самое новое',
          offers:
            [
              { id: 1, rating: { value: '4.6', count: '5' }, sticker: 'Скидка до 10%', img: 'image.jpg', title: 'Sale! Скидка 10%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: true },
              { id: 2, rating: { value: '3.6', count: '15' }, sticker: 'Скидка до 20%', img: 'image.jpg', title: 'Sale! Скидка 20%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 3, rating: { value: '5.0', count: '25' }, sticker: 'Скидка до 30%', img: 'image.jpg', title: 'Sale! Скидка 30%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 4, rating: { value: '4.7', count: '35' }, sticker: 'Скидка до 40%', img: 'image.jpg', title: 'Sale! Скидка 40%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false }
            ]
        },
        {
          id: 2,
          name: 'Максимально сэкономить',
          offers:
            [
              { id: 1, rating: { value: '4.6', count: '5' }, sticker: 'Скидка до 10%', img: 'image.jpg', title: 'Sale! Скидка 10%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 2, rating: { value: '3.6', count: '15' }, sticker: 'Скидка до 20%', img: 'image.jpg', title: 'Sale! Скидка 20%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 3, rating: { value: '5.0', count: '25' }, sticker: 'Скидка до 30%', img: 'image.jpg', title: 'Sale! Скидка 30%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 4, rating: { value: '4.7', count: '35' }, sticker: 'Скидка до 40%', img: 'image.jpg', title: 'Sale! Скидка 40%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false }
            ]
        },
        {
          id: 3,
          name: 'Популярное сегодня',
          offers:
            [
              { id: 1, rating: { value: '4.6', count: '5' }, sticker: 'Скидка до 10%', img: 'image.jpg', title: 'Sale! Скидка 10%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 2, rating: { value: '3.6', count: '15' }, sticker: 'Скидка до 20%', img: 'image.jpg', title: 'Sale! Скидка 20%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 3, rating: { value: '5.0', count: '25' }, sticker: 'Скидка до 30%', img: 'image.jpg', title: 'Sale! Скидка 30%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 4, rating: { value: '4.7', count: '35' }, sticker: 'Скидка до 40%', img: 'image.jpg', title: 'Sale! Скидка 40%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false }
            ]
        },
        {
          id: 4,
          name: 'Успеть в последний день',
          offers:
            [
              { id: 1, rating: { value: '4.6', count: '5' }, sticker: 'Скидка до 10%', img: 'image.jpg', title: 'Sale! Скидка 10%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 2, rating: { value: '3.6', count: '15' }, sticker: 'Скидка до 20%', img: 'image.jpg', title: 'Sale! Скидка 20%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 3, rating: { value: '5.0', count: '25' }, sticker: 'Скидка до 30%', img: 'image.jpg', title: 'Sale! Скидка 30%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false },
              { id: 4, rating: { value: '4.7', count: '35' }, sticker: 'Скидка до 40%', img: 'image.jpg', title: 'Sale! Скидка 40%!', companyName: 'Pizza Hot', geo: 'Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)', isFavorite: false }
            ]
        }
      ]
    }
  },

  methods: {

    toggleSeacrh() {
      if ((window.innerHeight + window.pageYOffset) >= document.body.offsetHeight) {
        this.isShort = true;
        return
      }
      if (window.scrollY <= 0) {
        this.isShort = false;
        return
      }
      if (this.positionY >= window.scrollY) {
        this.isShort = false;
      } else {
        this.isShort = true;
      }
      this.positionY = window.scrollY;
    }

  },

  computed: {
    isShow: function () {
      return this.isShort || !this.positionY === 0
    }
  }

}
</script>

<style>
</style>
