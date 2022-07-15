<template>
    <div class="container">
        <CardsComponent :CardsArray="cardsArray" />
    </div>
</template>

<script>
import mainCards from '../assets/json/mainCards.json';
import CardsComponent from './CardsComponent.vue';

export default {
    name: 'MainComponent',
    components: {
        CardsComponent
    },
    data() {
        return {
            cardsArray: mainCards
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';

</style>