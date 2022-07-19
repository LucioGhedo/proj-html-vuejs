<template>
    <div>
        <div class="top">
            <i class="fa-solid fa-angle-up"></i>
            <div>TOP</div>
        </div>
        <div class="container">
            <div class="flex">
                <div class="selection">
                    <!-- stampo le selection per tutti i link che abbiamo
                    e gli dico al click di invocare setCurrentActive() 
                    e ha sempre una classe dinamica per dire se è attivo o no -->
                    <div 
                    @click="setCurrentActive(index)"
                    v-for="item, index in links" 
                    :key="index" 
                    :class="currentActive === index ? 'active' : ''"
                    class="option">
                        {{item.text}}
                    </div>
                </div>
                <!-- qui stampo la pagina in base a ciò che abbiamo schiacciato nella selection
                e lo faccio sempre con la classe dinamica che lo nasconde o lo mostra in base all'index -->
                <div 
                v-for="items, index in pageElement" 
                :key="index" 
                class="selected"
                :class="currentActive === index ? '' : 'hidden'">
                    <h2>{{items.title}}</h2>
                    <p>
                        {{items.p}}
                    </p>
                    <p>
                        <i class="fa-solid fa-check"></i> 
                        {{items.check1}}
                    </p>
                    <p>
                        <i class="fa-solid fa-check"></i> 
                        {{items.check2}}
                    </p>
                    <p>
                        <i class="fa-solid fa-check"></i> 
                        {{items.check3}}
                    </p>
                    <p>
                        <i class="fa-solid fa-check"></i> 
                        {{items.check4}}
                    </p>
                    <img :src="require(`../assets/img/${items.img}`)" alt="img">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SelectionComponent',
    data() {
        return {
            currentActive: 1,
            links: [
                {
                    text: 'What we do'
                },
                {
                    text: 'Degree Programme'
                },
                {
                    text: 'Career Achievements'
                },
                {
                    text: 'Personal Managment'
                },
                {
                    text: 'Steps To Sucess'
                },
                {
                    text: 'Knowledge Transfer'
                }
            ],
            pageElement: [
                {
                    title: 'Learning Possibilities',
                    p: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, possimus eos placeat cumque beatae deserunt accusamus reprehenderit cum a nesciunt ipsam rerum eveniet aliquam labore eius ea? Magni, nesciunt. Enim.',
                    check1: 'We enrich lives through learning.',
                    check2: 'Maximizing potential through individual attention.',
                    check3: 'The trusted name for specializing training.',
                    check4: 'People teach. People learn. This is where they connect.',
                    img: 'h12-tabs-icon-1.png',
                },
                 {
                    title: 'Degree Programme',
                    p: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, possimus eos placeat cumque beatae deserunt accusamus reprehenderit cum a nesciunt ipsam umque beatae deserunt accusamus reprehenderit cum a nesciunt ipsam rerum eveniet aliquam labore eius ea? Magni, nesciunt. Enim.',
                    check1: 'We enrich lives through learning.',
                    check2: 'Maximizing potential through individual attention.',
                    check3: 'The trusted name for specializing training.',
                    check4: 'People teach. People learn. This is where they connect.',
                    img: 'h12-tabs-icon-2.png',
                },
                 {
                    title: 'Career Achievment',
                    p: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, possimus eos placeat cumque beatae deserunt accusamus reprehenderit cum a nesciunt ',
                    check1: 'We enrich lives through learning.',
                    check2: 'Maximizing potential through individual attention.',
                    check3: 'The trusted name for specializing training.',
                    check4: 'People teach. People learn. This is where they connect.',
                    img: 'h12-tabs-icon-3.png',
                },
                 {
                    title: 'Personal Managment',
                    p: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.  ipsam rerum eveniet aliquam labore eius ea? Magni, nesciunt. Enim.',
                    check1: 'We enrich lives through learning.',
                    check2: 'Maximizing potential through individual attention.',
                    check3: 'The trusted name for specializing training.',
                    check4: 'People teach. People learn. This is where they connect.',
                    img: 'h12-tabs-icon-4.png',
                },
                 {
                    title: 'Step to Success',
                    p: 'Hic, possimus eos placeat cumque beatae deserunt accusamus reprehenderit cum a nesciunt ipsam rerum eveniet aliquam labore eius ea? Magni, nesciunt. Enim.',
                    check1: 'We enrich lives through learning.',
                    check2: 'Maximizing potential through individual attention.',
                    check3: 'The trusted name for specializing training.',
                    check4: 'Ciao :)',
                    img: 'h12-tabs-icon-5.png',
                },
                 {
                    title: 'Knowledge Trasnfer',
                    p: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, possimus eos placeat cumque beatae deserunt accusamus reprehenderit cum a nesciunt ipsam rerum eveniet aliquam labore eius ea? Magni, nesciunt. Enim.',
                    check1: 'We enrich lives through learning.',
                    check2: 'Maximizing potential through individual attention.',
                    check3: 'The trusted name for specializing training.',
                    check4: 'People teach. People learn. This is where they connect.',
                    img: 'h12-tabs-icon-6.png',
                }
            ]
        }
    },
    methods: {
        // imposta currentactive = index di ciò che abbiamo cliccato
        setCurrentActive(index) {
            this.currentActive = index
            
        }
    }
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
    right: 0px;
}
.flex {
    justify-content: space-between;
}
.selection {
    width: calc(30% - 5px);
    .option {
        border: 1px solid lightgray;
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
        border-bottom: solid lightgray 1px;
    }
}
.hidden {
    display: none;
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