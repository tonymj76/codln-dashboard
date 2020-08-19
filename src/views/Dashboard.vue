<template>
  <div class="dashboard">
    <v-row>
      <v-col cols="12">
        <v-row
          align="center"
          justify="start"
        >
          <v-tabs
            v-model="tab"
            background-color="transparent"
            color='#F15832'
          >
            <v-tabs-slider color='#F15832'></v-tabs-slider>
            <v-tab
              v-for="i in tabs"
              :key="i"
              :href="`#tab-${i}`"
            >
              Tab {{i}}
            </v-tab>
            <v-tab-item
              v-for="i in tabs"
              :key="i"
              :value="'tab-' + i"
            >
              <v-card flat tile>
                <v-card-text>{{text}}</v-card-text>
              </v-card>
            </v-tab-item>
          </v-tabs>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>

export default {
  name: 'Dashboard',
  data() {
    return {
      tab: null,
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
      tabs: 3,
    };
  },
};
</script>

<style lang="scss" scoped>
</style>
