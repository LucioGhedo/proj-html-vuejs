<template>
    <header>
        <div class="container">
            <!-- NAVBAR -->
            <div class="navbar">
                <!-- LOGO -->
                <div class="logo">
                    <img src="../assets/img/logo-light.png" alt="Logo Icademy">
                </div>
                <!-- MENU LINK -->
                <div>
                    <a :href="item.link" v-for="item, index in headerLinks" :key="index">{{item.text}}</a>
                </div>
                <!-- ICONS -->
                <div class="icons">
                    <i class="fa-solid fa-magnifying-glass"></i>
                    <i class="fa-solid fa-bag-shopping"></i>
                    <div class="circle shop-circle">0</div>
                    <i class="fa-solid fa-bars"></i>
                </div>
            </div>
            <!-- FINE NAVBAR -->

            <!-- JUMBO -->
            <div class="text-center">
                <h3>Contemporary Ideas</h3>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsum vero reiciendis minus hic minima, eveniet ex repellendus adipisci maxime veritatis facilis quaerat blanditiis necessitatibus officia iure ab esse debitis assumenda.
                </p>
                <div class="btn jumbo-btn"><a href="#">REGISTER NOW</a></div>
                <div class="flex">
                    <!-- stampo i pallini (3) e al click richiamano la funzione setCurrentActive() e gli do una classe dinamica -->
                    <div 
                    @click="setCurrentActive(index)" 
                    v-for="item, index in 3" 
                    :key="item" 
                    class="circle jumbo-cirlce" 
                    :class="currentActive === index ? 'active' : '' ">
                        <!-- se currentactive = index stampo il pallino piccolo dentro per dire che è lui selezionato -->
                        <div v-if="currentActive === index" class="small-circle"></div>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            currentActive: 2,
        }
    },
    methods: {
        setCurrentActive(index) {
            this.currentActive = index;
        }
    },
    props: {
        headerLinks: Array,
    },
    
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
header {
    position: relative;
    height: 900px;
}
header::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%; height: 100%;
    background-image: url('../assets/img/course-9-f-img.jpg');
    filter: brightness(60%);
    background-size: 125%;
    background-position-x: -200px;
    background-repeat: no-repeat;
}
.container {
     position: relative;
}
.navbar {
    padding: 10px 0;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .icons {
        position: relative;
        i {
            padding: 0 4px;
            font-size: 16px;
            color: $text1;
        }
    }
    div {
        a {
            color: $text1;
            padding: 0 0.8vw;
            font-size: 1.5vw;
        }
    }
}
img {
    width: 100%;
}
.logo {
    width: 200px;
}
.jumbo-cirlce {
    width: 26px;
    height: 26px;
    padding: 10px;
    margin: 10px;
    margin-top: 70px;
    margin-bottom: 20px;
    text-align: center;
    position: relative;
    background-color: $back_2;
    &.active {
        border: solid white 3px;
        background-color: transparent;
        .small-circle {
            position: absolute;
            top: 6px;
            right: 5.6px;
            background-color: white;
            height: 9px;
            width: 9px;
            border-radius: 50%;
        }

    }
}
.flex {
    justify-content: center;
}
.shop-circle {
    background-color: $back_11;
    position: absolute;
    text-align: center;
    top: -3px;
    left: 31px;
    color: $text1;
    font-size: 10px;
}
.text-center {
    text-align: center;
    color: white;
}
h3 {
        padding-top: 15vw;
        font-size: 75px;
}
p {
    padding-top: 60px;
    font-size: 20px;
    line-height: 45px;
}
.btn {
    margin: 0 auto;
    padding: 25px;
    width: 200px;
    background-color: $back_11;
    margin-top: 50px;
    a {
        color: $text1;
    }
}
</style>