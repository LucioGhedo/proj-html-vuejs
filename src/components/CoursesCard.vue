<template>
<div class="flex">
    <div class="card" v-for="item, index in splicedArray" :key="index">
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
        json: Array,
        currentActive: Number,
    },
    data() {
        return {
            // le slides default con le quali la presentazione inizia
            splicedArray: [
                {
                    "title": "Android Developer",
                    "name": "David Sanders",
                    "tag": "PROGRAMMING",
                    "img": "course-2-f-img",
                    "price": "FREE"
                },
                {
                    "title": "Web Designer",
                    "name": "Jennifer Powell",
                    "tag": "PROGRAMMING",
                    "img": "course-8-f-img",
                    "price": "FREE"
                },
                {
                    "title": "Financial Modeling",
                    "name": "Edward Bowman",
                    "tag": "BUSINESS",
                    "img": "course-9-f-img",
                    "price": "$20"
                },
            ],
        }
    },
    methods: {
        // controllo il prezzo e restituisco un output vero/falso
        isFree(price) {
            if (price == 'FREE') {
                return true
            } else {
                return false
            }
        },
        // in base all'index del currentactive questa funzione accorcia l'array a 3 elementi e dice se mostrare i primi tre, i secondi o gli ultimi.
        slidesSplice() {
            if (this.currentActive == 1) {
                this.splicedArray = this.listJson.slice(0, 3);
            } else if (this.currentActive == 2) {
                this.splicedArray = this.listJson.slice(3, 6);
            } else if (this.currentActive == 0) {
                this.splicedArray = this.listJson.slice(6, 9);
            }
        }
    },
    // questa funzione rende modificabile il file json per poterlo usare nelle altre funzioni e lavorarci sopra
    computed: {
        listJson: function(){
            return JSON.parse(JSON.stringify(this.json));
        },
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