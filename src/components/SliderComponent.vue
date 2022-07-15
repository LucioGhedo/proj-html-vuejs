<template>
    <div class="back">
        <div class="container">
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
            setInterval(() => {
                if (this.currentActive < this.slidesArray.length - 1) {
                    this.currentActive ++
                } else if (this.currentActive === this.slidesArray.length - 1) {
                    this.currentActive = 0
                }
            }, 6000);
        },
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
}
.container {
    text-align: center;
    padding-top: 50px;
}
p {
    width: 80%;
    margin: 0 auto;
    padding: 20px 0;
    &.occupation {
        font-size: 10px;
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
    padding-bottom: 80px;
}
</style>