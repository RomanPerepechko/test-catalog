<template>

    <div @click="$emit('toggleFilter')" class="filter-btn" :class="{toggle: isSelect}">
        <img :src="require(`@/assets/${icon}`)" alt="">
        <span>{{ name }}</span>
    </div>

</template>

<script>

export default {

    props: {
        name: String,
        icon: String,
        isSelect: Boolean
    }

}
</script>

<style>
</style>