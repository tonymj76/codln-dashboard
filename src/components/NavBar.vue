<template>

  <v-app-bar
    app
    color="#FBFBFB"
    flat
  >
    <div class="d-flex align-center">
      <v-img
        alt="fcmb Logo"
        class="shrink mr-2"
        contain
        src="@/assets/img/logoname.svg"
      />
      <v-img
        alt="fcmb Logo"
        class="shrink line mr-2"
        contain
        src="@/assets/img/Line.svg"
      />
    </div>
    <v-input

          prepend-icon="mdi-magnify"
        >
          Search
        </v-input>
    <v-spacer></v-spacer>

    <v-btn
      href="https://github.com/vuetifyjs/vuetify/releases/latest"
      target="_blank"
      text
    >
      <span class="mr-2">Latest Release</span>
      <v-icon>mdi-open-in-new</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: 'NavBar',
};
</script>

<style lang="scss">
  $dark-blue: #03293D;
  .header__title {
    color : $dark-blue;
  }

  .line{
    margin-left: 43px !important;
  }

</style>
