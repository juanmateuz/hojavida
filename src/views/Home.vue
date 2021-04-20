<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/profile3.jpg" />
    <Perfil msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import Perfil from "@/components/Perfil.vue";

export default {
  name: "Home",
  components: {
    Perfil,
  },
};
</script>
