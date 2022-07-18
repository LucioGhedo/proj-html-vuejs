<template>
<div class="flex">
    <div class="card" v-for="item, index in json" :key="index">
        <img :src="require(`../assets/img/${item.img}.jpg`)" alt="img">
        <div class="text-container">
            <h4>{{item.title}}</h4>
            <span>{{item.name}}</span>
            <p>
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eligendi ab itaque dolorem facere, ipsum sint delectus alias beatae, aliquam illum, ipsa veniam aspernatur. Corporis laudantium ducimus quae, pariatur in obcaecati!
            </p>
            <div class="icons">
                <i class="fa-solid fa-user"></i>
                <span>1</span>
                <i class="fa-solid fa-tag"></i>
                <span>{{item.tag}}</span>
            </div>
        </div>
        <div class="price" :class="isFree(item.price) ? 'orange' : 'blue'">{{item.price}}</div>
    </div>    
</div>
</template>

<script>
export default {
    name: 'CoursesCard',
    props: {
        json: Array
    },
    methods: {
        isFree(price) {
            if (price == 'FREE') {
                return true
            } else {
                return false
            }
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
.flex {
    justify-content: space-between;
}
.card {
    background-color: $back_1;
    width: calc((100% / 3) - 20px);
    border: solid lightgray 1px;
    position: relative;
    .text-container {
        padding: 5px 10px;
    }
    img {
        width: 100%;
    }
    h4 {
        padding: 10px 0;
    }
    span {
        color: $text2;
    }
    p {
        color: $text3;
        padding: 10px 0;
    }
    i {
        color: $text3;
        padding: 0 10px;
    }
    .price {
        color: $text1;
        position: absolute;
        padding: 2px 9px;
        border-radius: 5px;
        top: 50%;
        right: 10px;
    }
}
.orange {
    background-color: $back_9;
}
.blue {
    background-color: $back_11;
}
</style>