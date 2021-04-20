<template>
  <v-layout row>
    <!-- open card -->
    <v-row class="margin justify-start mb-3 font">
      <v-col class="margin">
        <v-dialog transition="dialog-bottom-transition" max-width="700">
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              class="boton"
              small
              outlined
              color="teal"
              v-bind="attrs"
              v-on="on"
              @click="open($event)"
              >Open Proyect
            </v-btn>
          </template>
          <!-- close card -->
          <template v-slot:default="dialog">
          <!--card -->
            <v-card>
              <v-toolbar color="secondary" dark class="font"
                >Software Mantenimiento</v-toolbar
              >
              <v-carousel
                hide-delimiters
                width="400"
                height="auto"
                hide-delimiter-background
                show-arrows-on-hover
                class="carousel"
              >
                <!-- visualización imagenes -->
                <v-carousel-item
                  class="img"
                  v-for="(item, i) in items"
                  :key="i"
                >
                  <div
                    id="div1"
                    class="d-flex flex-column justify-space-between align-center"
                  >
                    <v-img :src="item.src" class="img"></v-img>
                  </div>
                </v-carousel-item>
              </v-carousel>
              <!--accion -->
              <v-card-actions class="justify-end">
                <v-btn text @click="dialog.value = false">Cerrar</v-btn>
              </v-card-actions>
              <!--fin accion -->
            </v-card>
          </template>
        </v-dialog>
      </v-col>
    </v-row>
  </v-layout>
</template>
<script>
export default {
  name: "Carousel",

  props: ["numero"],

  data() {
    return {
      num: this.numero,
      items: [],
    };
  },
  methods: {
    open() {
      if (this.num == 1) {
        this.items = [
          {
            src: require("../assets/Mto/software.jpg"),
          },
          {
            src: require("../assets/Mto/diag.jpg"),
          },
          {
            src: require("../assets/Mto/software3.jpg"),
          },
          {
            src: require("../assets/Mto/soft.jpg"),
          },
        ];
      } else {
        this.items = [
          {
            src: require("../assets/Mto/ecommerce.jpg"),
          },
          {
            src: require("../assets/Mto/ecommerce2.jpg"),
          },
        ];
      }
    },
  },
};
</script>

<style scoped>
/* margen columna card */
.margin {
  margin-top: 0;
  margin: 0px 0px 0px 38px;
  padding: 0px 0px 0px 0px;
}
/* estilo letra */
.font {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
/* estilo imagen */
.img {
  width: 100%;
  max-width: 700px;
  height: auto;
  padding: 0px 0px 0px 0px;
}
.carousel {
  width: "200px";
  height: "200px";
}
.boton {
  padding: 0px 0px 0px 0px;
}
</style>