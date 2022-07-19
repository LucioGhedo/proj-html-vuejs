<template>
    <div class="back">
        <div class="top">
            <a href="#">
                <i class="fa-solid fa-angle-up"></i>
                <div>TOP</div>
            </a>
        </div>
        <div class="container">
            <div class="col-container">
                <div class="col">
                    <img src="../assets/img/footer-logo-1.png" alt="logo">
                    <p class="gray">
                        Providing Life Changing Experiences Throught Education.
                        Class That Fit Your Busy Life. Closer to Home
                    </p>
                    <div class="row">
                        <i class="fa-solid fa-phone"></i>
                        1-234-567-890
                    </div>
                    <div class="row">
                        <i class="fa-solid fa-clock"></i>
                        Mon - Sat 8:00 18:00
                    </div>
                </div>
                <div class="col">
                    <h3>Popular Courses</h3>
                    <!-- stampo un elemento (item) per ogni oggetto dell'array (firstList) -->
                    <div v-for="item, index in firstList" :key="index" class="text hovereffect">
                        <div class="title">
                            {{item.title}}
                        </div>
                        <span class="text8">
                            {{item.name}}
                        </span>
                    </div>
                </div>
                <div class="col">
                    <h3>Support</h3>
                    <!-- stampo un elemento (item) per ogni oggetto dell'array (secondList) -->
                    <div v-for="items, index in secondList" :key="index" class="text text8 hovereffect">
                        <div>
                            {{items.support}}
                        </div>
                    </div>
                </div>
                <div class="col">
                    <h3>Flexible learning</h3>
                    <img src="../assets/img/footer-img-1.png" alt="map" class="map">
                </div>
            </div>
            <hr>
            <div class="bottom-footer">
                <div class="height">
                    Copyright 2022 &copy; Lucio Ghedina
                </div>
                <div class="height">
                    CALL +39 346 4134953
                    <span class="height">FOLLOW US</span>
                    <span class="height">
                        <i class="fa-brands fa-instagram"></i>
                        <i class="fa-brands fa-facebook"></i>
                        <i class="fa-brands fa-twitter"></i>
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterComponent',
    // le liste arrivano come props sotto forma di array
    props: {
        firstList: Array,
        secondList: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
* {
    color: $text2;
}
h3 {
    color: $text1;
}
p {
    padding-top: 20px;
}
.back {
    background-color: $back_15;
    position: relative;
}
img {
    width: 80%;
}
.col-container {
    display: flex;
    justify-content: space-between;
}
.col {
    padding-top: 80px;
    padding-bottom: 90px;
    width: calc((100% / 4) - 10px);
}
.row {
    padding: 15px 0;
}
.text {
    margin: 20px 0;
}
.title {
    font-size: 18px;
}
.text8 {
    color: $text8;
}
.map {
    margin-top: 20px;
}
.height {
    line-height: 80px;
    color: $text8;
}
.bottom-footer {
    display: flex;
    justify-content: space-between;
    i {
        padding: 0 10px;
    }
    span {
        padding: 0 10px;
    }
}
.top {
    position: absolute;
    bottom: 50px;
    right: 0;
    a {
        display: flex;
        flex-direction: column;
        align-items: center;
        i {
            color: $text1;
        }
        div {
            color: $text1;
        }
    }
}
.hovereffect {
    padding: 5px;
    width: fit-content;
}
.hovereffect:hover {
    background-color: $back_3;
    border-radius: 5px;
    padding: 5px;
    width: fit-content;
    div {
        color: $text4;
    }
    span {
        color: $text4;
    }
}
.gray {
    color: gray;
}
</style>