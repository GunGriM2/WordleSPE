<template>
  <v-app>
    <Header/>
    <router-view style="top: 80px"/>
  </v-app>
</template>

<script>
import Header from "@/components/Header";
import {Component, Vue} from "vue-property-decorator";
import UserService from "@/services/UserService";

@Component({
  components: {
    Header
  }
})
export default class App extends Vue{

}

</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
