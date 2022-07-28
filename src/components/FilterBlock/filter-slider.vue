<template>

    <div class="filter-slider">

        <filter-btn 
        @toggle-filter="() => { filter.isSelect = !filter.isSelect }" 
        v-for="filter in filters" 
        :key="filter.id"
        :name="filter.name" 
        :icon="filter.icon" 
        :isSelect="filter.isSelect"
        />

    </div>

</template>

<script>
import FilterBtn from './filter-btn.vue';

export default {

    data() {
        return {
            filters: [
                { id: 1, name: 'Подборки', icon: 'test.svg', isSelect: false },
                { id: 1, name: 'Все категории', icon: 'test.svg', isSelect: false },
                { id: 1, name: 'Где поесть', icon: 'test.svg', isSelect: false },
                { id: 1, name: 'Где сэкономить', icon: 'test.svg', isSelect: false },
                { id: 1, name: 'Где отдохнуть', icon: 'test.svg', isSelect: false }
            ]
        }
    },

    components: {
        FilterBtn
    }

}
</script>

<style>
</style>