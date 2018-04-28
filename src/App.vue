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
        this.component = tab;
        document.querySelector('body').className = '';
        document.querySelector('body').classList.add(tab);
      }
    }
  }
</script>

<style lang="scss">
body {
  padding-left: 150px;
  background-color: #596770;
  background: url(./assets/intro-bg.png) no-repeat center center fixed;
  background-size: cover;
}
#app {
  // font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #e2e2e2;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
