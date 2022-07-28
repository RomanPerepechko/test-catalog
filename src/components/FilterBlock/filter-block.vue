<template>
    <div class="filter-block" :style="isShort ? 'height:70px;' : null">
        <search-input></search-input>
        <filter-slider></filter-slider>
    </div>
</template>

<script>
import SearchInput from '../UI/SeacrhInput/search-input.vue';
import FilterSlider from './filter-slider.vue'

export default {
    props: {
        isShort: Boolean
    },
    components: {
        SearchInput,
        FilterSlider
    }
}
</script>

<style scoped>
.filter-block {
    position: sticky;
    height: 140px;
    background-color: white;
    width: 100vw;
    top: 0px;
    z-index: 9999;
    transition: all .2s cubic-bezier(0, 0, 1, 1);
    box-shadow: 2px 2px 8px rgb(0 0 0 / 10%);
    overflow: hidden;
}
</style>