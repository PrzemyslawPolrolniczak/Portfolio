<template>
  <div id="app">
    <navbar-component></navbar-component>
    <img src="./assets/logo.png">
    <h1>{{ title }}</h1>
    <h2>{{ subtitle }}</h2>
  </div>
</template>

<script>
  import PageHeadingComponent from './PageHeadingComponent.vue'
  import StaffListComponent from './StaffListComponent.vue'
  import NavbarComponent from './NavbarComponent.vue'

  export default {
    name: 'app',
    components: {NavbarComponent, PageHeadingComponent, StaffListComponent},
    data () {
      return {
        title: 'Przemysław Półrolniczak',
        subtitle: 'Junior Front-end Developer',
      }
    }
  }
</script>

<style lang="scss">
body {
  padding-left: 150px;
  background-color: #596770;
  // background-color: #7C8B95
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
