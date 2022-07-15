<template>
  <div id="app">
    <HeaderComponent :headerLinks="headerLink" />
    <MainComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'

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
      ]
    }
  },
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent
},
}
</script>

<style lang="scss">
@import './assets/style/common.scss';
</style>
