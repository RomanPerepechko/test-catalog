<template>
    <div class="promo-card">
        <div class="promo-card__img">
            <img src="@/assets/image.jpg" alt="" class="">
            <div class="promo-card__rating">4,6(5)</div>
            <div class="promo-card__sticker-discount">Скидка до 30%</div>
        </div>
        <div class="promo-card__title">Sale! Скидка 30%!</div>
        <div class="promo-card__body">
            <div class="promo-card__description">
                <div class="promo-card__company-name">Pizza Hot</div>
                <div class="promo-card__geo">Ближайшее: Ростов-на-Дону, пойменная улица, 1 (1,9км)</div>
            </div>
            <button class="promo-card__like-btn">лайк</button>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.promo-card__sticker-discount{
    position: absolute;
    left:5px;
    top: -10px;
    height: 20px;
    background-color: orange;
}
.promo-card__rating{
    position: absolute;
    left:5px;
    bottom: 5px;
    background-color: white;
    box-shadow: 2px 2px 8px rgb(0 0 0 / 10%);
    border-radius: 8px;
    width: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
}
.promo-card {
    height: 400px;
    width: 300px;
    min-width: 300px;
    border-radius: 8px;
    box-shadow: 2px 2px 8px rgb(0 0 0 / 10%);
    margin: 10px;
    /* убрать маргин */
}

.promo-card__img {
    width: 100%;
    max-height: 250px;
    border-radius: 8px;
    position: relative;
}
.promo-card__img img{
    object-fit: cover;
    width: 100%;
    max-height: 250px;
    border-radius: 8px;
}
.promo-card__body {
    padding: 12px;
}

.promo-card__title {
    margin: 12px 0px 12px 12px;
}

.promo-card__body {
    display: flex;
}
</style>