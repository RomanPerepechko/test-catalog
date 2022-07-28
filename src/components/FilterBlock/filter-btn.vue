<template>

    <div @click="$emit('toggleFilter')" class="filter-btn" :style="isSelect ? 'background-color:#30d5c8;color:#fff;' : null">
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