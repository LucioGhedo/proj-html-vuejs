<template>
    <div class="back">
        <div class="container">
            <img src="../assets/img/testimonials-standard-2.png" alt="testimonials">
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. In eius optio aperiam ea praesentium. Facilis ipsam sequi architecto maiores dolorem! Neque eveniet quam dolorem omnis aspernatur amet. Accusantium, neque debitis.</p>
            <h4>Joe Collins</h4>
            <p class="occupation">STUDENT</p>
            <div class="flex-circles">
                <div class="circle white"></div>
                <div class="circle white active"></div>
                <div class="circle white"></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SliderComponent',
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