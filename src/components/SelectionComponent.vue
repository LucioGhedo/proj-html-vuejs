<template>
    <div class="container">
        <div class="top">
            <i class="fa-solid fa-angle-up"></i>
            <div>TOP</div>
        </div>
        <div class="flex">
            <div class="selection">
                <div class="option active">What We Do</div>
                <div class="option">Degree Programme</div>
                <div class="option">Career Achievements</div>
                <div class="option">Personal Managment</div>
                <div class="option">Steps To Sucess</div>
                <div class="option">Knowledge Transfer</div>
            </div>
            <div class="selected">
                <h2>Learning Possibilities</h2>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, possimus eos placeat cumque beatae deserunt accusamus reprehenderit cum a nesciunt ipsam rerum eveniet aliquam labore eius ea? Magni, nesciunt. Enim.
                </p>
                <p>
                    <i class="fa-solid fa-check"></i> 
                    We enrich lives through learning.
                </p>
                <p>
                    <i class="fa-solid fa-check"></i> 
                    Maximizing potential through individual attention.
                </p>
                <p>
                    <i class="fa-solid fa-check"></i> 
                    The trusted name for specializing training.
                </p>
                <p>
                    <i class="fa-solid fa-check"></i> 
                    People teach. People learn. This is where they connect.
                </p>
                <img src="../assets/img/h12-tabs-icon-1.png" alt="img">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SelectionComponent',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
.container {
    padding-top: 80px;
    padding-bottom: 100px;
}
.top {
    position: absolute;
    top: 30px;
    right: -80px;
}
.flex {
    justify-content: space-between;
}
.selection {
    width: calc(30% - 5px);
    .option {
        border: 1px solid grey;
        border-bottom: none;
        line-height: 80px;
        text-align: center;
        font-weight: 900;
        color: grey;
        &.active {
            color: $text4;
            border-left: 10px solid $back_11;
            background-color: $back_5;
        }
    }
    .option:last-of-type {
        border-bottom: solid grey 1px;
    }
}
.selected {
    position: relative;
    width: calc(70% - 5px);
    padding: 20px 40px;
    p {
        color: $text3;
        font-size: 18px;
        line-height: 29px;
        padding: 15px 0;
    }
    img {
        position: absolute;
        bottom: 0;
        right: 0;
        width: 100px;
    }
}
i {
    color: $text4;
    padding: 0 5px;
}
</style>