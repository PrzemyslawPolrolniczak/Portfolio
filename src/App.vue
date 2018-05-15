<template>
  <div id="app">
    <navbar-component v-on:changeTab="updateView($event)"></navbar-component>
    <component :is="component"></component>
  </div>
</template>

<script>
  import PageHeadingComponent from './PageHeadingComponent.vue'
  import IntroComponent from './IntroComponent.vue'
  import NavbarComponent from './NavbarComponent.vue'
  import AboutComponent from './AboutComponent.vue'
  import ContactComponent from './ContactComponent.vue'
  import LinksComponent from './LinksComponent.vue'
  import ProjectsComponent from './ProjectsComponent.vue'

  export default {
    name: 'app',
    components: {NavbarComponent, PageHeadingComponent, IntroComponent, AboutComponent, ContactComponent, LinksComponent, ProjectsComponent},
    data () {
      return {
        component: 'intro-component',
      }
    },
    methods: {
      updateView(tab) {
        this.component = tab[0];
        document.querySelector('body').className = '';
        document.querySelector('body').classList.add(tab);
      }
    }
  }
</script>

<style lang="scss">
@import './scss/variables.scss';
#app {
  transition: background-color 0.5s;
  position: absolute;
  margin-left: 150px;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  background: url(./assets/intro-bg.png) no-repeat center center fixed;
  background-color: #31373c;
  background-size: cover;
  // font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #e2e2e2;
  &.blue {
      background: rgba($color: #D6C5A7, $alpha: 1.0);
  }
  &.red {
      background: rgba($color: #B8B499, $alpha: 1.0);
  }
  &.green {
      background: rgba($color: #98A886, $alpha: 1.0);
  }
  &.yellow {
      background: rgba($color: #787B5C, $alpha: 1.0);
  }
}

h1, h2 {
  font-weight: normal;
}
</style>
