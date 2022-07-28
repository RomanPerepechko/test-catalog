<template>

    <div class="promo-card">

        <div class="promo-card__img">
            <img :src="require(`@/assets/${offer.img}`)" alt="" class="">
            <div class="promo-card__rating">{{ offer.rating.value }}({{ offer.rating.count }})</div>
            <div class="promo-card__sticker-discount">{{ offer.sticker }}</div>
        </div>

        <div class="promo-card__title">{{ offer.title }}</div>

        <div class="promo-card__body">

            <div class="promo-card__description">
                <div class="promo-card__company-name">{{ offer.companyName }}</div>
                <div class="promo-card__geo">{{ offer.geo }}</div>
            </div>

            <svg @click="$emit('toggleFavorite')" width="32" height="32" viewBox="0 0 24 21" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M1.89964 5.07419C2.16348 4.43723 2.5502 3.85847 3.03771 3.37096C3.52522 2.88345 4.10398 2.49673 4.74094 2.23289C5.37791 1.96905 6.0606 1.83325 6.75005 1.83325C7.43949 1.83325 8.12219 1.96905 8.75915 2.23289C9.39611 2.49673 9.97487 2.88345 10.4624 3.37096L12 4.90863L13.5377 3.37096C14.5223 2.38639 15.8577 1.83327 17.25 1.83327C18.6424 1.83327 19.9778 2.38639 20.9624 3.37096C21.947 4.35554 22.5001 5.6909 22.5001 7.0833C22.5001 8.47569 21.947 9.81106 20.9624 10.7956L12 19.758L3.03771 10.7956C2.5502 10.3081 2.16348 9.72936 1.89964 9.0924C1.6358 8.45544 1.5 7.77274 1.5 7.0833C1.5 6.39385 1.6358 5.71116 1.89964 5.07419Z"
                    :stroke="offer.isFavorite ? 'red' : 'black'" :fill="offer.isFavorite ? 'red' : 'none'" stroke-width="2" stroke-linecap="round"
                    stroke-linejoin="round" />
            </svg>

        </div>
        
    </div>

</template>

<script>
export default {

    props: {
        offer: Object
    }

}
</script>

<style></style>