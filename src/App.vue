<template>
  <div id="app">
    <HeaderComponent :headerLinks="headerLink" />
    <main>
      <MainComponent />
    </main>
    <footer>
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
