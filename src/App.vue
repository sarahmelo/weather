<template>
  <v-app>
    <v-nav-bar>
      <v-toolbar dense flat>
        <v-title>Weather</v-title>
      </v-toolbar>
    </v-nav-bar>
    <v-main>
      <v-col>
        <Search
          :apiWeather="locationData"
          :city="city"
          :response="apiResponse"
        />
        <Display :weatherResponse="apiResponse" />
      </v-col>
    </v-main>
  </v-app>
</template>

<script>
import Search from "./components/Search";
import Display from "./components/Display";

export default {
  name: "App",

  components: {
    Search,
    Display,
  },

  data: () => ({
    apiResponse: [],
    city: "",
  }),

  methods: {
    async locationData() {
      let response = await fetch(
        `https://api.openweathermap.org/data/2.5/weather?q=${this.city},${this.state},br&lang=pt_br&units=metric&appid=bff4ad52bd5c29357f5626257723a26b`
      );
      this.apiResponse = await response.json();
      console.log(this.apiResponse);
    },
  },
};
</script>

<style>
v-nav-bar {
  border-left: 6px solid #ff6987;
}

v-title {
  font-family: "Righteous", cursive;
  font-size: larger;
}
</style>
