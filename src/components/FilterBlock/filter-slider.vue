<template>
    <div class="filter-slider">
        <filter-btn @toggle-filter="() => { filter.isSelect = !filter.isSelect }" v-for="filter in filters" :key="filter.id"
            :name="filter.name" :icon="filter.icon" :isSelect="filter.isSelect"/>
    </div>
</template>

<script>
import FilterBtn from './filter-btn.vue'
export default {
    data() {
        return {
            filters: [
                { id: 1, name: 'test', icon: 'test', isSelect: false },
                { id: 1, name: 'test', icon: 'test', isSelect: false },
                { id: 1, name: 'test', icon: 'test', isSelect: false },
                { id: 1, name: 'test', icon: 'test', isSelect: false },
                { id: 1, name: 'test', icon: 'test', isSelect: false }
            ]
        }
    },
    components: {
        FilterBtn
    }
}
</script>

<style scoped>
::-webkit-scrollbar {
    width: 0px;
    background: transparent;
}

html {
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.filter-slider {
    display: flex;
    overflow: scroll;
    height: 70px;
}
</style>