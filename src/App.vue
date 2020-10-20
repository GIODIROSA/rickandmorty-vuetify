<template>
  <v-app>
    <Navbar />
    <CardsCharacter />
    <v-main> </v-main>
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import CardsCharacter from "./components/CardsCharacter.vue";

export default {
  name: "App",
  components: {
    Navbar,
    CardsCharacter,
  },

  data: () => ({
    //
  }),
};
</script>
