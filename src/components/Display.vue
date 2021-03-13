<template>
  <v-col>
    <v-card>temperatura atual</v-card>

    <v-col> colunas com próximas temperaturas </v-col>
  </v-col>
</template>

<script>
export default {
  name: "display",
  prop: {
    info: String,
  },
};
</script>

<style>
</style>