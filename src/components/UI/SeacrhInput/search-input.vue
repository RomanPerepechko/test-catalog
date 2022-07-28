<template>
    <div class="search-input">
        <input type="text" placeholder="Поиск по всем категориям">
        <div class="search-input__icon">
            <img src="@/assets/search-icon.svg" alt="">
        </div>
    </div>

</template>

<script>
export default {

}
</script>

<style scoped>
.search-input__icon{
    position: absolute;
    right: 30px;
    height: 16px;
    width: 16px;
}
.search-input__icon img{
    object-fit: cover;
    height: 100%;
    width: 100%;
}
.search-input {
    width: 100vw;
    height: 36px;
    padding: 0px 8px 0px 8px;
    display: flex;
    align-items: center;
    margin: 16px 0px 16px 0px;
    position: relative;
}

.search-input input {
    width: calc(100% - 64px);
    height: 100%;
    background: #FFFFFF;
    border: 1px solid #C5C0C0;
    border-radius: 6px;
    outline: none;
    padding: 0px 24px 0px 24px;
}
</style>