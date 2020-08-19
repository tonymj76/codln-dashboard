<template>
  <v-app>
    <NavBar />
    <v-main class="main">
      <v-container>
        <router-view></router-view>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import NavBar from './components/NavBar.vue';

export default {
  name: 'App',

  components: {
    NavBar,
  },

  data: () => ({
    //
  }),
};
</script>

<style lang="scss">
 .main{
   background: #E5E5E5;
 }

</style>
