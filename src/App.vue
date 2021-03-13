<template>
  <v-app>
    <v-main>
      <v-col>
        <Search />
        <Display />
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

  data: () => ({}),
};
</script>

<style>
body {
  height: 100vh;
  width: 100vw;
}
</style>
