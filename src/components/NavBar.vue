<template>
  <nav>
    <v-app-bar
    flat
    app
    color="#FBFBFB"
    height="86"
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
    :mini-variant="miniVariant"
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

      <v-divider class="mb-5" ></v-divider>

      <v-list-item
        v-for="navItem in navItems"
        :key="navItem.title"
        link
      >
        <v-list-item-action class="mb-5" router :to="navItem.route">
          <v-img
          alt="menu"
          :src="navItem.url"
        />
        </v-list-item-action>
      </v-list-item>

      <v-divider class="my-5"></v-divider>
      <v-list-item
        v-for="navFab in navFabButtons"
        :key="navFab.color"
        link
      >
        <v-list-item-action class="mb-1">
          <v-btn fab x-small :color="navFab.color" depressed>
            {{navFab.title}}
          </v-btn>
        </v-list-item-action>
      </v-list-item>

    </v-list>
      <v-divider class="my-5" ></v-divider>
    <template v-slot:append>
        <div class="pa-2 mb-8">
          <v-btn class="mx-2 " fab depressed color="#f8f5fd6b">
        <v-icon dark color="#23B3E8" size='40'>mdi-chevron-right</v-icon>
      </v-btn>
        </div>
      </template>
  </v-navigation-drawer>
  </nav>
</template>

<script>
import home from '@/assets/img/home.svg';
import link from '@/assets/img/link.svg';
import share from '@/assets/img/share.svg';

export default {
  name: 'NavBar',
  data() {
    return {
      drawer: false,
      expandOnHover: false,
      color: '#052231',
      miniVariant: true,
      items: {
        avatar: 'https://cdn.vuetifyjs.com/images/lists/2.jpg',
        title: '<span class="dark--text text--lighten-4">Chioma Davis</span>',
        email: "<span class='blue--text text--lighten-2'>Chioma@natterbar</span>",
      },

      navItems: [
        {
          title: 'Home', url: home, alt: 'home', route: '/',
        },
        {
          title: 'navigate', url: link, alt: 'link', route: '#',
        },
        {
          title: 'share', url: share, alt: 'people', route: '#',
        },
      ],
      navFabButtons: [
        {
          title: 'PN', color: '#23B3E8',
        },
        {
          title: 'JI', color: '#4DBD98',
        },
        {
          title: 'LG', color: '#3D43A2',
        },
        {
          title: 'AW', color: '#F15832',
        },
        {
          title: 'AW', color: '#004F71',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scope>
  $dark-blue: #03293D;
  $nav-color: #f8f5fd6b;
  .n__color{
    background: &$nav-color !important;
  }
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
