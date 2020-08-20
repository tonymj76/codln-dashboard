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
            <v-tab
              v-for="tabName in tabs"
              :key="tabName"
            >
              {{tabName}}
            </v-tab>

          </v-tabs>
          <v-tabs-items v-model="tab" class="mt-10">
            <v-tab-item>
              <v-card flat tile>
                <v-card-text>
                  Overview
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                  sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                  Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
                  nisi ut aliquip ex ea commodo consequat.
                </v-card-text>
              </v-card>
            </v-tab-item>
            <v-tab-item>
              <v-card flat tile>
                <v-card-text>
                Teams
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                  sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                  Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
                  nisi ut aliquip ex ea commodo consequat.
                </v-card-text>
              </v-card>
            </v-tab-item>
            <v-tab-item>
              <v-card flat tile>
                <v-card-text>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                  sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                  Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
                  nisi ut aliquip ex ea commodo consequat.
                </v-card-text>
              </v-card>
            </v-tab-item>
            <v-tab-item>
              <Module />
            </v-tab-item>
            <v-tab-item>
              <v-card flat tile>
                <v-card-text>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                  sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                  Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
                  nisi ut aliquip ex ea commodo consequat.
                </v-card-text>
              </v-card>
            </v-tab-item>
          </v-tabs-items>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Module from '@/components/Module.vue';

export default {
  name: 'Dashboard',
  components: {
    Module,
  },
  data() {
    return {
      tab: null,
      tabs: [
        'Overview', 'Teams', 'Test', 'Modules', 'Progress',
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
</style>
