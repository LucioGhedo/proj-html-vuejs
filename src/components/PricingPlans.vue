<template>
    <div class="back">
        <div class="cart">
            <img class="cart-img" src="../assets/svg/svg-2.svg" alt="cart">
        </div>
        <div class="circle-red">
            <img class="circle-img" src="../assets/svg/svg-0.svg" alt="cirlce?">
        </div>
        <div class="top">
            <i class="fa-solid fa-angle-up"></i>
            <div>TOP</div>
        </div>
        <div class="container">
            <div class="center">
                <h2>Pricing Plans</h2>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Asperio
                </p>
            </div>
            <div class="flex">
                <!-- col 1 -->
                <div class="col">
                    <!-- title -->
                    <div class="firstcol-card">
                        <h3>Save up to 40% by paying weekly</h3>
                    </div>
                    <div class="card-2 grey weight">Number of courses</div>
                    <div class="card-2 grey weight">Time</div>
                    <div class="card-2 grey weight">Web Designing</div>
                    <div class="card-2 grey weight">Human-Centered Design</div>
                    <div class="card-2 grey weight">Basic Marketing</div>
                    <div class="card-2 grey weight">Python for Everybody</div>
                    <div class="card-2 grey weight">Android Developer</div>
                    <div class="card-2 grey weight">Business English</div>
                </div>
                <!-- col 2 -->
                <div class="col">
                    <!-- img title -->
                    <div class="firstcol-card textcenter color">
                        <img src="../assets/img/h5-custom-icon-7.png" alt="lens">
                        <h4>Standard</h4>
                        <div class="price">12$</div>
                    </div>
                    <div class="card textcenter">
                        2
                    </div>
                    <div class="card textcenter">
                        15
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card textcenter grey">
                        <i class="fa-solid fa-x"></i>
                    </div>
                    <div class="card textcenter grey">
                        <i class="fa-solid fa-x"></i>
                    </div>
                    <div class="card textcenter grey">
                        <i class="fa-solid fa-x"></i>
                    </div>
                    <div class="card first textcenter btn-card">
                        <div class="btn grey-btn">
                            <a href="#">GET IT NOW</a>
                        </div>
                    </div>
                </div>
                <!-- col 3 -->
                <div class="col">
                    <!-- img title -->
                    <div class="firstcol-card textcenter color active">
                        <img src="../assets/img/h5-custom-icon-8.png" alt="brain">
                        <h4>Professional</h4>
                        <div class="price">59$</div>
                    </div>
                    <div class="card textcenter">
                        4
                    </div>
                    <div class="card textcenter">
                        30
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card textcenter grey">
                        <i class="fa-solid fa-x"></i>
                    </div>
                    <div class="card textcenter grey">
                        <i class="fa-solid fa-x"></i>
                    </div>
                    <div class="card textcenter btn-card">
                        <div class="btn blue-btn">
                            <a href="#">GET IT NOW</a>
                        </div>
                    </div>
                </div>
                <!-- col 4 -->
                <div class="col">
                    <!-- img title -->
                    <div class="firstcol-card textcenter color">
                        <img src="../assets/img/h5-custom-icon-9.png" alt="hat">
                        <h4>Advanced</h4>
                        <div class="price">88$</div>
                    </div>
                    <div class="card textcenter">
                        6
                    </div>
                    <div class="card textcenter">
                        30
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card textcenter blue">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <div class="card btn-card textcenter">
                        <div class="btn grey-btn">
                            <a href="#">GET IT NOW</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'PricingPlans',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
.back {
    position: relative;
    background-image: url('../assets/img/page-background-img.png');
}
.top {
    position: absolute;
    top: 200px;
    right: 0;
}
.price {
    font-weight: 900;
    margin-bottom: 15px;
}
.textcenter {
    text-align: center;
}
.center {
    text-align: center;
    margin-top: 90px;
    p {
        width: 70%;
        margin: 0 auto;
        padding: 20px 0;
        color: $text8;
        font-size: 18px;
    }
}
.color {
    background-color: $back_8;
}
.col {
    width: calc((100% / 4) - 15px);
    background-color: $back_1;
    margin-bottom: 90px;
    height: fit-content;
    h3 {
        margin-top: 130px;
        margin-bottom: 30px;
        padding: 0 15px;
    }
    h4 {
        margin-bottom: 10px;
    }
    img {
        margin-top: 25px;
    }
    .firstcol-card {
        border-right: solid lightgray 1px;
        border-bottom: solid lightgray 1px;
        border-top: solid $back_10 5px;
        &.active {
            border-top: solid $back_11 5px;
        }
    }
    .firstcol-card:first-of-type {
        border-left: solid lightgray 1px;
    }
}
.card {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 50px;
    border-bottom: solid lightgray 1px;
    border-right: solid lightgray 1px;
}
.first {
    border-left: solid lightgray 1px;
}
.card-2 {
    display: flex;
    align-items: center;
    height: 40px;
    padding: 0 10px;
    border-bottom: solid lightgray 1px;
    border-right: solid lightgray 1px;
    border-left: solid lightgray 1px;
}
.blue {
    color: $text4;
}
.grey {
    color: $text8;
}
.weight {
    font-weight: 800;
}
.btn {
    padding: 9px 20px;
}
.blue-btn {
    background-color: $back_11;
    color: $text1;
}
.grey-btn {
    background-color: $back_3;
    border: solid $text8 1px;
}
.btn-card {
    height: 90px;
    background-color: $back_8;
}
.cart {
    .cart-img {
        width: 35px;
        padding: 8px;
        background-color: $back_1;
        position: absolute;
        top: 120px;
        right: 0;
    }
}
.circle-red {
    .circle-img {
        width: 35px;
        padding: 8px;
        background-color: $back_12;
        color: $text1;
        position: absolute;
        top: 80px;
        right: 0;
    }
}
</style>