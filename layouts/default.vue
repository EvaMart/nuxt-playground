<template>
  <v-app dark>
    <v-main>
      <v-toolbar class="pb-2" elevation="1">
        <h2>OEB Visualizations Demo</h2>

        <v-spacer></v-spacer>
        <v-btn
          icon
          href="http://github.com/inab/oeb-visualizations-demo"
          target="_blank"
        >
          <v-icon>mdi-github</v-icon>
        </v-btn>

        <v-divider
          class="mx-4 ml-1"
          inset
          vertical
        ></v-divider>

        <v-switch
          v-model="$vuetify.theme.dark"
          inset
          dense
          hide-details
        >
        <template v-slot:label>
          <v-icon>mdi-theme-light-dark</v-icon>
        </template>
      </v-switch>
      </v-toolbar>
        <Nuxt />
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
      class="text-center"
    >
      <span> </span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      fixed: false,
    }
  }
}
</script>
