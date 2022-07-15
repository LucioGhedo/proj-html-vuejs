<template>
    <div class="container">
        <section>
            <CardsComponent :CardsArray="cardsArray" />
        </section>
        <section>
            <TrustedSection />
        </section>
    </div>
</template>

<script>
import mainCards from '../assets/json/mainCards.json';
import CardsComponent from './CardsComponent.vue';
import TrustedSection from './TrustedSection.vue';

export default {
    name: 'MainComponent',
    components: {
    CardsComponent,
    TrustedSection
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
.container {
    position: relative;
}
</style>