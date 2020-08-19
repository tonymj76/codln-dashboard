<template>

  <v-app-bar
    flat
    app
    color="#FBFBFB"
  >
    <div class="d-flex align-center">
      <v-img
        alt="fcmb Logo"
        class="shrink mr-2"
        contain
        src="@/assets/img/logoname.svg"
      />
      <v-img
        alt="line"
        class="shrink line mr-2"
        contain
        src="@/assets/img/Line.svg"
      />
      <v-text-field
          hide-details
          prepend-icon="mdi-magnify"
          solo
          flat
          label="Search"
        ></v-text-field>
    </div>
    <v-spacer></v-spacer>
    <div class="d-flex align-center">
          <v-badge
      color="#E13071"
      dot
      overlap
    >
    <v-icon>mdi-bell-outline</v-icon>
    </v-badge>
    <v-img
        alt="owner"
        class="shrink ml-6"
        contain
        src="@/assets/img/owner.svg"
      />
    <v-img
        alt="tag"
        class="shrink ml-6"
        contain
        src="@/assets/img/tag.svg"
      />
      <v-list class="ml-6" dense flat>
        <v-list-item>
          <v-list-item-avatar>
            <v-img :src="items.avatar"></v-img>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title v-html="items.title"></v-list-item-title>
            <v-list-item-title v-html="items.email"></v-list-item-title>
          </v-list-item-content>
          <v-list-item-icon>
            <v-icon right>mdi-chevron-down</v-icon>
          </v-list-item-icon>
        </v-list-item>
      </v-list>
    </div>
  </v-app-bar>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      items: {
        avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
        title: '<span class="dark--text text--lighten-4">Chioma Davis</span>',
        email: "<span class='blue--text text--lighten-2'>Chioma@natterbar</span>",
      },
    };
  },
};
</script>

<style lang="scss" scope>
  $dark-blue: #03293D;
  .header__title {
    color : $dark-blue;
  }
  .v-list-item__icon:last-of-type:not(:only-child) {
   margin-left: 0 !important;
  }
  .line{
    margin-left: 43px !important;
  }
  .custom-box{
    width: 74px;
    height: 21px;
    background: linear-gradient(0deg, #4DBD98, #4DBD98),
    linear-gradient(0deg, #4DBD98, #4DBD98), linear-gradient(0deg, #4DBD98, #4DBD98),
    #4DBD98;
    border-radius: 5px;
  }

</style>
