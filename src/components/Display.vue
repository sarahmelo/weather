<template>
  <v-col>
    <v-card>temperatura atual</v-card>
    <!-- {{ this.todo }} -->
    <v-col> colunas com próximas temperaturas </v-col>
  </v-col>
</template>

<script>
export default {
  name: "display",
  props: {
    weatherResponse: Array,
  },
};
</script>

<style>
</style>