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
            <PricingPlans />
        </section>
        <section>
            <SponsorSection />
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
import PricingPlans from './PricingPlans.vue';
import SponsorSection from './SponsorSection.vue';

export default {
    name: 'MainComponent',
    components: {
    CardsComponent,
    TrustedSection,
    SecondSection,
    SliderComponent,
    SelectionComponent,
    PopularCouses,
    PricingPlans,
    SponsorSection
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