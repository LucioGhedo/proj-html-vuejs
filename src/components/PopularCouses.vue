<template>
    <div class="back">
        <div class="container">
            <div class="center">
                <h2>Popular Online Courses</h2>
                <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Asperiores incidunt quae minima ipsam quis cupiditate corporis
                </p>
            </div>
            <!-- dentro a popularcourses stampo le slides di coursescard e gli passo con i props chi è attivo e il file json -->
            <CoursesCard :json="cardJson" :currentActive="currentActive" />
        </div>
        <div class="circle-container">
            <!-- stampo i tre pallini su cui posso selezionare le slize e al click richiamo
            setCurrentActive() e slidesSplice() che è una funzione del figlio, uso
            $children[0] per dirgli che la funzione la trova nel componente figlio -->
            <div 
            v-for="n, index in 3" 
            :key="n" 
            @click="setCurrentActive(index), $children[0].slidesSplice()" 
            :class="currentActive == index ? 'active' : ''" 
            class="circle">
            </div>
        </div>
        <div class="top">
            <i class="fa-solid fa-angle-up"></i>
            <div>TOP</div>
        </div>
    </div>
</template>

<script>
import CourseCard from '../assets/json/courseCard.json';
import CoursesCard from './CoursesCard.vue';
export default {
    name: "PopularCourses",
    components: { CoursesCard },
    data() {
        return {
            cardJson: CourseCard,
            currentActive: 0,
        }
    },
    methods: {
        setCurrentActive(index) {
            this.currentActive = index;
        },
        // di default l'elemento attivo è 0
        setZero() {
            this.currentActive = 0;
        }
    },
    // funzioni che partono al mounted
    mounted() {
        this.setCurrentActive();
        this.setZero();
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
.back {
    border-top: solid lightgray 1px;
    border-bottom: solid lightgray 1px;
    background-image: url('../assets/img/page-background-img.png');
    padding-bottom: 90px;
    position: relative;
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
.circle-container {
    display: flex;
    justify-content: center;
}
.circle {
    background-color: $back_10;
    margin: 50px 5px;
    &.active {
        background-color: $back_11;
    }
}
.top {
    position: absolute;
    right: 0;
    bottom: 230px;
}
</style>