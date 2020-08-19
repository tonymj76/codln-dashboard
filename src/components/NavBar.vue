<template>
  <nav>
    <v-app-bar
    flat
    app
    color="#FBFBFB"
  >
    <div class="d-flex align-center">
      <v-app-bar-nav-icon class="menu__icon" @click="drawer = !drawer">
        <v-img
          alt="menu"
          class="shrink"
          contain
          src="@/assets/img/menu.svg"
        />
    </v-app-bar-nav-icon>
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
      <v-list class="ml-6" dense flat color="#FBFBFB">
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
  <v-navigation-drawer
    app
    floating
    v-model="drawer"
    :color="color"
    :expand-on-hover="expandOnHover"
    mini-variant
    mini-variant-width="96"
    permanent
    absolute
    dark
  >
    <v-list
      dense
      nav
      class="py-0"
    >
      <v-list-item two-line :class="miniVariant && 'px-0'">
        <v-list-item-avatar>
          <img src="@/assets/img/logo.svg" alt="codeln logo">
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title>CodLn</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list-item>
        <v-list-item-icon>
        </v-list-item-icon>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      drawer: false,
      expandOnHovor: false,
      color: '#052231',
      items: {
        avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
        title: '<span class="dark--text text--lighten-4">Chioma Davis</span>',
        email: "<span class='blue--text text--lighten-2'>Chioma@natterbar</span>",
      },

      navItems: [
        { title: 'Home', url: '@/assets/img/home.svg', alt: 'home' },
        { title: 'navigate', url: '@/assets/img/link.svg', alt: 'link' },
        { title: 'share', url: '@/assets/img/people.svg', alt: 'people' },
      ],
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
  .menu__icon{
    margin-left: 25px;
    margin-right: 41px;
  }

</style>
