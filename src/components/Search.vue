<template>
  <v-col cols="6" class="d-inlind-flex flex-row">
    <v-row class="justify-space-around">
      <v-text-field
        label="Rio de Janeiro"
        solo
        append-icon="mdi-send-circle"
        dark
        rounded
        v-model="city"
        @click:append="locationData()"
      ></v-text-field>
      <!-- <v-btn color="indigo" v-on:click="locationData()">click</v-btn> -->
    </v-row>
    <br />
    <!-- {{ this.apiResponse }} -->
    <v-spacer></v-spacer>
  </v-col>
</template>

<script>
export default {
  name: "search",
  props: {
    apiWeather: [Function, Promise],
    city: String,
    response: Array,
  },
  data: () => {
    // return {
    //   todo: {},
    //   city: "",
    //   state: "",
    // };
  },
  methods: {
    clearInput() {
      this.city = "";
    },
  },
};
</script>

<style>
</style>