<template>
  <!-- color de fondo hoja vida -->
  <v-app style="background: #dee3e4">
    <v-app-bar app dark>
      <v-spacer></v-spacer>
      <v-btn href="https://github.com/juanmateuz" target="_blank" text>
        <span class="mr-2">DEVELOPER</span>
        <v-icon>fas fa-external-link-alt</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <Perfil />
    </v-main>
  </v-app>
</template>

<script>
import Perfil from "./components/Perfil.vue";

export default {
  name: "App",
  components: {
    Perfil,
  },
  data: () => ({
    //
  }),
};
</script>