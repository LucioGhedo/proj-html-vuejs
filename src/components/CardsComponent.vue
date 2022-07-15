<template>
    <div class="card-container">
        <div class="card" v-for="item, index in CardsArray" :key="index">
            <img :src="require(`../assets/img/${item.img}.png`)" :alt="item.text">
            <span class="text">{{item.text}}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CardsComponent',
    props: {
        CardsArray: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
.card-container {
    display: flex;
    margin: 40px 0;
}
.card {
    background-color: $back_8;
    width: calc(99% / 5);
    height: 150px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin: 0 10px;
    border: solid $back_4 1px;
    img {
        width: 70px;
        padding-bottom: 15px;
    }
    .text {
        font-weight: 800;
    }
}

</style>