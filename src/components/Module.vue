<template>
  <div>
      <v-card flat>
    <v-toolbar
      color="#E5E5E5"
      flat
    >
      <v-toolbar-title>Backlog</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-dots-horizontal</v-icon>
      </v-btn>
    </v-toolbar>
  </v-card>
  <v-card flat>
    <v-btn icon>
        <v-icon>mdi-dots-horizontal</v-icon>
      </v-btn>
  </v-card>
  </div>
</template>

<script>
export default {
  name: 'Module',
  data: () => ({
    items: [
      { title: 'Click Me' },
      { title: 'Click Me' },
      { title: 'Click Me' },
      { title: 'Click Me 2' },
    ],
  }),
};
</script>

<style lang="scss" scoped>

</style>
