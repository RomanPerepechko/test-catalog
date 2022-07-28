<template>

    <div class="filter-block" :class="{show: isShort}" >

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

<style>
</style>