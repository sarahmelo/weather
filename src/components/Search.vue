<template>
  <v-col cols="6" class="d-inlind-flex flex-row">
    <v-row class="justify-space-around">
      <v-text-field
        v-model="city"
        label="Search for city"
        hide-details
      ></v-text-field>

      <v-text-field
        v-model="state"
        label="Search for state"
        hide-details
      ></v-text-field>
      <v-btn color="indigo" v-on:click="locationData()">click</v-btn>
    </v-row>
    <br />
    {{ this.todo }}
    <v-spacer></v-spacer>
    <Display :weatherData="todo" />
  </v-col>
</template>

<script>
import Display from "./Display";
export default {
  name: "search",
  props: {},
  components: {
    Display,
  },
  data: () => {
    return {
      todo: {},
      city: "",
      state: "",
    };
  },
  methods: {
    async locationData() {
      let response = await fetch(
        `https://api.openweathermap.org/data/2.5/weather?q=${this.city},${this.state},br&lang=pt_br&units=metric&appid=bff4ad52bd5c29357f5626257723a26b`
      );
      this.todo = await response.json();
      console.log(this.todo);
    },
  },
};
</script>

<style>
</style>