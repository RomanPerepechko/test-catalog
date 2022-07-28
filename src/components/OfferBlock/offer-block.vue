<template>

    <div class="offer-block">

        <div class="offer-block__title">
            <div class="offer-block__name">"{{name}}"</div>
            <div class="offer-block__btn-all">Смотреть все</div>
        </div>
        
        <div class="offer-block__slider">
            <promo-card @toggle-favorite="()=>{offer.isFavorite = !offer.isFavorite}" v-for="offer in offers" :key="offer.id" :offer="offer"></promo-card>
        </div>

    </div>

</template>

<script>
import PromoCard from '@/components/PromoCard/promo-card.vue';

export default {

    components: {
        PromoCard
    },

    props:{
        name: String,
        offers : Array
    }

}
</script>

<style>
</style>