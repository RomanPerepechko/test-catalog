<template>
  <div @wheel="toggleSeacrh" class="container">

    <filter-block 
    :isShort="isShort"
    >

    </filter-block>

    <offer-block 
    v-for="block in blocks" 
    :key="block.id" 
    :name="block.name" 
    :offers="block.offers">

    </offer-block>

  </div>
</template>

<script>
import FilterBlock from '@/components/FilterBlock/filter-block.vue';
import OfferBlock from '@/components/OfferBlock/offer-block.vue';
export default {
  components: {
    OfferBlock,
    FilterBlock
  },
  data() {
    return {
      isShort: false,
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

    toggleSeacrh(ev) {
      if (ev.deltaY < 0) {
        this.isShort = false;
      } else {
        this.isShort = true;
      }
    }

  }

}
</script>

<style>
* {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 0px;
  padding: 0px;
}

.container {
  display: flex;
  flex-direction: column;
  position: relative;
}
</style>
