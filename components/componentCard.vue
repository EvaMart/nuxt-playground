<template>
    <v-col cols="12" sm="10" md="10">
        <v-card class="pl-8 pr-8 pb-4 mt-4">
          <v-card-title><a :href="documentationLink" target="_blank">{{ title }}</a></v-card-title>
          <component :is="componentToDisplay" />
        </v-card>
     </v-col>

</template>
<script>

export default {
  name: 'ComponentCard',
  props: {
    componentToDisplay: {
      type: String,
      required: true
    },
    documentationLink: {
      type: String,
      required: false,
      default: ''
    },
    title: {
      type: String,
      required: true
    }
  }
}

</script>