<template>
  <v-app>
  <Nav/>
  <Home/>
  </v-app>
</template>

<script>
import Nav from './components/TheNav.vue';
import Home from './views/Home.vue';
export default {
  components:{Nav,Home}
}
</script>
