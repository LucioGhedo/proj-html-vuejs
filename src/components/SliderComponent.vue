<template>
    <div class="back">
        <div class="container">
            <!-- stampo una slide per ogni elemento di slidesarray -->
            <!-- e gli do una classe dinamica che in base all'index dell elemento nasconde o mostra la singola slide -->
            <div 
            v-for="item, index in slidesArray" 
            :key="index"
            :class="currentActive === index ? '' : 'hidden'">
                <img :src="require(`../assets/img/${item.img}`)" alt="testimonials">
                <p>{{item.text}}</p>
                <h4>{{item.name}}</h4>
                <p class="occupation">{{item.occupation}}</p>
            </div>
            <div class="flex-circles">
                <!-- stampo i pallini sempre con classe dinamica relativa all'index per le slide
                 e al click sopra richiamano selectThis() -->
                <div 
                v-for="items, index in slidesArray" 
                :key="index" 
                class="circle white"
                :class="currentActive === index ? 'active': ''"
                @click="selectThis(index)">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import slides from '../assets/json/slidesJson.json';

export default {
    name: 'SliderComponent',
    methods: {
        setCurrentActive() {
            // faccio un setinterval per scorrere le slides in automatico
            setInterval(() => {
                // incremento currentactive finchè è minore a slidesarray
                if (this.currentActive < this.slidesArray.length - 1) {
                    this.currentActive ++
                } 
                // se currentactive è uguale a slidesarray lo riporto a zero
                 else if (this.currentActive === this.slidesArray.length - 1) {
                    this.currentActive = 0
                }
            }, 6000);
        },
        // seleziona la slide attiva in base al click dell'utente
        selectThis(index) {
            this.currentActive = index
        }
    },
    data() {
        return {
            slidesArray: slides,
            currentActive: 0,
        }
    },
    // al created faccio partire il setinterval
    created() {
        this.setCurrentActive();
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
.back {
    background-color: $back_11;
    background-image: url('../assets/img/interactive-map-slider-img-1.png');
    color: $text1;
    height: 400px;
}
.container {
    text-align: center;
    padding-top: 50px;
}
p {
    width: 80%;
    margin: 0 auto;
    padding: 20px 0;
    height: 90px;
    &.occupation {
        font-size: 10px;
        height: fit-content;
    }
}
.hidden {
    display: none;
}
.white {
    background-color: #aadbf1;
    margin: 0 5px;
    &.active {
        background-color: white;
    }
}
.flex-circles {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>