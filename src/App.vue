<template>
  <v-app class="bg-color"> 
    <Navbar  />
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

  import Navbar from './components/Navbar.vue';

  export default {
    name: 'App',
    components : {
      Navbar,
    },

    data () {
       //
    },
  }
</script>

<style>

.bg-color {
  background-color: rgb(238, 237, 240) !important;
}

.app-container {
  max-width: 1320px !important;
  margin-left: auto;
  margin-right: auto;
}
</style>