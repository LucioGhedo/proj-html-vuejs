<template>
    <div>
        <div class="container">
            <div class="flex">
                <div class="half">
                    <img src="../assets/img/h8-slide-1-img.png" alt="World">
                </div>
                <div class="half">
                    <h2>Empowering Children to Reach their Potential.</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eaque quae animi itaque placeat quos labore fugit reiciendis quasi recusandae, error cumque amet maiores incidunt minima nam voluptate vitae debitis aut.</p>
                    <div class="flex color-cont">
                        <div class="color">
                            <div>156</div>
                            <div class="small">User Stories</div>
                        </div>
                        <div class="color">
                            <div>356</div>
                            <div class="small">Events</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="top">
            <i class="fa-solid fa-angle-up"></i>
            <a href="#">
                <div>TOP</div>
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SecondSection',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
img {
    width: 100%;
}
a {
    text-decoration: none;
    color: inherit;
}
h2 {
    padding: 40px 0;
    width: 80%;
    margin: 0 auto;
}
p {
    width: 80%;
    margin: 0 auto;
    font-size: 20px;
}
.half {
    width: calc((100% / 2) - 20px);
    margin-bottom: 50px;
}
.color-cont {
    width: 78%;
    margin: 0 auto;
    justify-content: space-between;
    padding-top: 30px;
}
.color {
    font-size: 30px;
    font-weight: 700;
    color: $text4;
}
.small {
    font-size: 20px;
}
.top {
    position: absolute;
    right: 0;
    top: 80%;
}
</style>