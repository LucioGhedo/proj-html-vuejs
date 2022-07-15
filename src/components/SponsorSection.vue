<template>
    <div class="border">
        <div class="contain">
            <div class="img-container">
                <img src="../assets/img/h5-client-5.png" alt="iacademy">
                <img src="../assets/img/h5-client-1.png" alt="study central">
                <img src="../assets/img/h5-client-2.png" alt="educator">
                <img src="../assets/img/h5-client-1.png" alt="study central">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SponsorSection',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
.border {
    border-top: 1px solid lightgray;
}
.img-container {
    margin: 40px 0;
    img {
        width: calc((100% / 4) - 5px);
    }
}
</style>