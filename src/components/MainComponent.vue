<template>
    <div>
        <div class="container">
            <section>
                <CardsComponent :CardsArray="cardsArray" />
            </section>
            <section>
                <TrustedSection />
            </section>
            <section>
                <SecondSection />
            </section>
        </div>

        <SliderComponent />
        <section>
            <SelectionComponent />
        </section>
        <section>
            <PopularCouses />
        </section>
        <section>
            
        </section>
    </div>
</template>

<script>
import mainCards from '../assets/json/mainCards.json';
import CardsComponent from './CardsComponent.vue';
import TrustedSection from './TrustedSection.vue';
import SecondSection from './SecondSection.vue';
import SliderComponent from './SliderComponent.vue';
import SelectionComponent from './SelectionComponent.vue';
import PopularCouses from './PopularCouses.vue';

export default {
    name: 'MainComponent',
    components: {
    CardsComponent,
    TrustedSection,
    SecondSection,
    SliderComponent,
    SelectionComponent,
    PopularCouses
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
section {
    position: relative;
}
</style>