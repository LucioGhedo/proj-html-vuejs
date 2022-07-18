<template>
    <div class="back">
        <div class="container">
            <h2>The trusted Name for In-Home tutoring. </h2>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Eos consequatur, dicta, magnam omnis ut officia amet excepturi fugiat debitis molestiae impedit error minima ab veritatis, sed nisi esse dolorem nostrum.</p>
            <div>
                <a href="#">LEARN MORE</a>
            </div>
            <img src="../assets/img/Capture.jpg" alt="foto">
        </div>
        <div class="top">
            <i class="fa-solid fa-angle-up"></i>
            <div>TOP</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TrustedSection',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
.back {
    border-bottom: solid lightgray 1px;;
}
h2 {
    width: 44%;
}
p {
    color: grey;
    margin: 15px 0;
}
a {
    font-size: 15px;
    color: $text4;
}
.top {
    position: absolute;
    right: -0;
    top: 50%;
}
img {
    width: 100%;
}
</style>