<template>
  <div id="app">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <HeaderComponent :headerLinks="headerLink" />
    <main>
      <MainComponent />
    </main>
    <footer>
      <!-- passo come props le liste che andranno a popolare questa area -->
      <FooterComponent :firstList="popularCoursesFooter" :secondList="support" />
    </footer>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import FooterComponent from './components/FooterComponent.vue'

export default {
  data() {
    return {
      headerLink: [
        {
          text: 'HOME',
          link: '#',
        },
        {
          text: 'COURSES',
          link: '#',
        },
        {
          text: 'INSTRUCTOR',
          link: '#',
        },
        {
          text: 'EVENTS',
          link: '#',
        },
        {
          text: 'PAGES',
          link: '#',
        },
        {
          text: 'ELEMENTS',
          link: '#',
        },
      ],
      popularCoursesFooter: [
        {
          title: 'Business English',
          name: 'Preston Marshall'
        },
        {
          title: 'Social Computing',
          name: 'David Sanders'
        },
        {
          title: 'Learn Spanish',
          name: 'Jennie King'
        }
      ],
      support: [
        {
          support: 'User dashboard'
        },
        {
          support: 'Contact US'
        },
        {
          support: 'FAQ'
        },
        {
          support: 'Course offer'
        },
        {
          support: 'Events'
        }
      ]
    }
  },
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent
},
}
</script>

<style lang="scss">
@import './assets/style/common.scss';
@import url("https://fonts.googleapis.com/css?family=Roboto+Condensed");
</style>
