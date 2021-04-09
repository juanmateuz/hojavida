<template>
   <v-app style="background: #DEE3E4"><!--color="#38AEEA" -->
    <v-app-bar
      app      
      dark
    >   
      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/juanmateuz"
        target="_blank"
        text
      >
        <span class="mr-2">DEVELOPER</span>
        <v-icon>fas fa-external-link-alt</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';


export default {
  name: 'App',

  components: {
    HelloWorld
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
app{
  background: #DEE3E4
}
</style>