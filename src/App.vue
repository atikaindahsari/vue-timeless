<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      flat
    >
    <Header/>
    </v-app-bar>

    <router-view></router-view>

    <v-main>
      <Hero/>
      <Gallery/>
      <LatestPost/>
    </v-main>
    <v-footer>
      <Footer/>
    </v-footer>
  </v-app>

</template>

<script>
import Header from "./components/common/Header";
import Footer from "./components/common/Footer";

export default {
  name: "App",

  components: {
    Header,
    Footer
  },

  data: () => ({
    //
  })
};
</script>
