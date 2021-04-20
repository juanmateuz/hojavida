<template>
  <v-card class="mx-auto my-7" max-width="900">
    <v-app id="inspire">
      <v-container class="my-1">
        <v-layout row>
          <!-- información personal -->
          <v-flex xs12 sm4 md3 order-lg2>
            <div
              id="div1"
              class="d-flex flex-column justify-space-between align-center"
            >
              <v-img width="25rem" height="18rem" src="../assets/profile3.jpg">
              </v-img>
            </div>
            <div class="name d-flex flex-column">
              <h2 class="ml-2 titulos">Juan David Mateus</h2>
              <p class="ml-3 titulos">Full Stack Developer</p>
            </div>

            <div class="d-flex flex-column justify-space-between contacto">
              <h3 class="my-2 ml-2">Contacto</h3>
              <h4 class="my-1 ml-3 titulos">
                <i class="fab fa-whatsapp fa-lg"></i> +57(310)3844660
              </h4>
              <h4 class="my-1 ml-3 titulos">
                <i class="far fa-envelope fa-lg"></i> juanmateuz@gmail.com
              </h4>
            </div>

            <div class="d-flex flex-column justify-space-between contacto">
              <h3 class="my-2 ml-2 titulos">Perfil</h3>
              <h4 class="my-1 ml-4 titulos">
                <i class="fab fa-linkedin fa-lg"></i
                ><a href="https://www.linkedin.com/in/juan-david-mateus-a003a117a/" target="_blank" class="titulos ml-1" style="color:white"
                  >LinkedIn</a
                >
              </h4>
              <h4 class="my-1 ml-4 titulos">
                <i class="fab fa-github fa-lg"></i> 
                <a href="https://github.com/juanmateuz" target="_blank" class="titulos ml-1" style="color:white"
                  >Github</a>
              </h4>
            </div>

            <div class="d-flex flex-column justify-space-between">
              <h3 class="my-2 ml-2 titulos">Habilidades</h3>
              <hr />
              <h4 class="my-1 ml-2 titulos">
                <i class="fab fa-angular fa-lg ml-3" style="color: #bf0011"></i>
                Angular
              </h4>
              <div class="lineProgress">
                <v-progress-linear value="35" height="8" color="#434e5e">
                </v-progress-linear>
              </div>
              <h4 class="my-1 ml-2 titulos">
                <i class="fab fa-vuejs fa-lg ml-3" style="color: #1d5201"></i>
                Vue js
              </h4>
              <div class="lineProgress">
                <v-progress-linear
                  value="40"
                  height="8"
                  color="#434E5E"
                ></v-progress-linear>
              </div>
              <h4 class="my-1 ml-2 titulos">
                <i
                  class="fab fa-cuttlefish fa-lg ml-3"
                  style="color: #4b026d"
                ></i
                ><strong>#</strong> .Net Core
              </h4>
              <div class="lineProgress">
                <v-progress-linear
                  value="35"
                  height="8"
                  color="#434E5E"
                ></v-progress-linear>
              </div>
              <h4 class="my-1 ml-2 titulos">
                <i
                  class="fab fa-cuttlefish fa-lg ml-3"
                  style="color: #4b026d"
                ></i
                ><strong>#</strong> .Net Framework
              </h4>
              <div class="lineProgress">
                <v-progress-linear
                  value="35"
                  height="8"
                  color="#434E5E"
                ></v-progress-linear>
              </div>
              <h4 class="my-1 ml-2 titulos">
                <i class="fab fa-html5 fa-lg ml-3" style="color: #e14d03"></i>
                HTML
              </h4>
              <div class="lineProgress">
                <v-progress-linear
                  value="35"
                  height="8"
                  color="#434E5E"
                ></v-progress-linear>
              </div>
              <h4 class="my-1 ml-2 titulos">
                <i
                  class="fab fa-css3-alt fa-lg ml-3"
                  style="color: #1c90e6"
                ></i>
                CSS
              </h4>
              <div class="lineProgress">
                <v-progress-linear
                  value="35"
                  height="8"
                  color="#434E5E"
                ></v-progress-linear>
              </div>
            </div>
            <hr class="mt-5" />
            <div class="d-flex flex-column justify-space-between">
              <h3 class="ml-2 titulos">Curriculum</h3>
              <h4 class="my-2 ml-2 titulos">
                <i
                  class="fas fa-file-pdf fa-lg ml-3"
                  style="color: #bd1717"
                ></i>
                <a href="hvjuan.pdf" target="_blank" class="boton"
                  >Download curriculum</a
                >
              </h4>
            </div>
            <!-- <a href="hvjuan.pdf" target="_blank">download pdf</a>-->
          </v-flex>
          <!-- fin informacion personal -->
          <v-flex xs12 sm8 md9>
            <v-card tile flat>
              <v-card-text>
                <i class="far fa-address-card fa-2x ml-8 my-1"
                  ><strong class="ml-1 titulos">PERFIL</strong></i
                >
                <p class="texto mr-3">
                  Ingeniero Informático de la Universidad de Caldas, con
                  competencias de trabajo en equipo, comunicación efectiva,
                  visión integral de negocio, inteligencia emocional, capacidad
                  para enfrentar retos y alcanzar metas con estrategias
                  innovadoras, con una gran curiosidad por aprender tecnologías
                  que faciliten el desarrollo.
                </p>
              </v-card-text>
            </v-card>
            <!-- Experiencia -->
            <Experiencia />
          </v-flex>
        </v-layout>
      </v-container>
    </v-app>
  </v-card>
</template>

<script>
import Experiencia from "./Experiencia";
import Proyectos from "./Proyectos";
import pdf from "vue-pdf";

export default {
  name: "HelloWorld",
  components: {
    Experiencia,
    Proyectos,
    pdf,
  },
  data: () => ({
    modulosMto: [
      "Modulo repuestos",
      "Modulo Proveedores",
      "Modulo Costos",
      "Modulo Mantenimiento",
      "Modulo Informes",
    ],
    perfil: "",
  }),
  methods: {
    print() {
      console.log("Imprimir");
      var pdf = "../assets/pdf/hvjuan.pdf";
      window.open(pdf); //to open in new tab
    },
  },
};
</script>

<style scoped>
.name {
  color: white;
  background-color: #434e5e;
}
.contacto {
  background-color: #c04212; /*#F68308 */
  color: white; /*#D7DBDD */
}
.cardPrincipal {
  box-shadow: 0 0 0 2em #f4aab9, 0 0 0 4em #66ccff;
  margin: 4em;
  padding: 1em;
}
/* texto pagina */
.texto {
  color: #463f3f;
  margin: 0px 20px 0px 30px;
  text-align: justify;
  font-size: 16px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
.lineProgress {
  margin-left: 20px;
  margin-right: 15px;
}
.styleProgress {
  color: #434e5e;
}
.titulos {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
.boton {
  padding: 0px 0px 0px 0px !important;
  margin: 0px 0px 0px 4px !important;
  color: #212121 !important;
}
a:hover,
a:visited,
a:link,
a:active {
  text-decoration: none;
}
</style>