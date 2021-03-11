<template>
  <v-app>
    <v-main>
      <Search />
      <Display />
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
    //
  }),
};
</script>
