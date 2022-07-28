<template>
    <div @click="$emit('toggleFilter')" class="filter-btn" :style="isSelect ? 'background-color:#30d5c8;color:#fff;' : null">
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

<style scoped>
.filter-btn {
    height: 36px;
    min-width: 100px;
    border-radius: 8px;
    box-shadow: 2px 2px 8px rgb(0 0 0 / 10%);
    margin: 8px;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    border: 1px solid #C5C0C0;
    color: #C5C0C0;
}

.filter-btn img {
    height: 16px;
    width: 16px;
}
</style>