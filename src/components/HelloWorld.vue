<template>
  <v-card class="mx-auto my-7" max-width="900">
    <v-app id="inspire" >    
      <v-container  class="my-1 ">
        <v-layout row>
          <v-flex xs12 sm4  md3 order-lg2  >
              <div id="div1" class="d-flex flex-column justify-space-between align-center" >        
                <v-img                                                             
                   width="25rem"
                    height="18rem"
                    src="../assets/profile3.jpg">
                </v-img>            
            </div>
            <div class="name d-flex flex-column">				
              <h2 class="ml-2" >Juan David Mateus</h2>
               <p class="ml-3">Full Stack Developer</p>
                    
                         
            </div>

            <div class="d-flex flex-column justify-space-between contacto">
              <h3 class="my-2 ml-2">CONTACTO</h3>          
              <h4 class="my-1"><i class="fab fa-whatsapp fa-lg ml-3"></i> + 57(310)3844660</h4>
              <h4 class="my-1"><i class="far fa-envelope fa-lg ml-3"></i> juanmateuz@gmail.com</h4>
            </div>
                  
            <div class="d-flex flex-column justify-space-between contacto">
              <h3 class="my-2 ml-2">PERFIL</h3>   
              <h4 class="my-1 "><i class="fab fa-linkedin fa-lg ml-4"></i> LinkedIn</h4>
              <h4 class="my-1 "><i class="fab fa-github fa-lg ml-4"></i> GitHub</h4> 
            </div>

            <div class="d-flex flex-column justify-space-between contacto">
              <h3 class="my-2 ml-2">CURRICULUM</h3> 
              <h4 class="my-1 "><i class="far fa-file-pdf fa-lg ml-3"></i> Formato Impresión</h4>              
            </div> 

            <div class="d-flex flex-column justify-space-between">              
              <h3 class="my-5 ml-2">Habilidades</h3> 
                 <hr>
              <h4 class="my-1"><i class="fab fa-angular fa-lg ml-3" style="color:#BF0011"></i> Angular</h4>
              <h4 class="my-1"><i class="fab fa-vuejs fa-lg ml-3" style="color:#1D5201"></i> Vue js</h4>    
              <h4 class="my-1"><i class="fab fa-cuttlefish fa-lg ml-3" style="color:#4B026D"></i><strong>#</strong> .Net Core</h4>      
              <h4 class="my-1"><i class="fab fa-cuttlefish fa-lg ml-3" style="color:#4B026D"></i><strong>#</strong> .Net Framework</h4>  
              <h4 class="my-1"><i class="fab fa-html5 fa-lg ml-3" style="color:#E14D03 "></i> HTML</h4>                                              
              <h4 class="my-1"><i class="fab fa-css3-alt fa-lg ml-3" style="color:#1C90E6"></i> CSS</h4>                                                                                          
            </div> 
          </v-flex>

          <v-flex xs12 sm8 md9>
            <v-card tile flat >
              <v-card-text >         
                <i class="far fa-address-card fa-2x ml-10 my-1"><strong class="ml-3">PERFIL</strong></i>                  
                  <v-list-item class="ml-6">
                    Ingeniero Informático de la Universidad de Caldas, con competencias de trabajo en equipo, 
                    comunicación efectiva, visión integral de negocio, inteligencia emocional, 
                    capacidad para enfrentar retos y alcanzar metas con estrategias innovadoras,                 
                    con una gran curiosidad por aprender tecnologías que faciliten 
                    el desarrollo.
                  </v-list-item>              
              </v-card-text>
            </v-card>
           <!-- Experiencia -->  
           <main>
               <Experiencia/> 
           </main>         
                     
           <!--Fin -->          
          </v-flex>
        </v-layout>
        <!-- <v-layout row>
          <v-flex xs4 order-md2 order-xs1>
            <v-card dark tile flat color="red lighten-1">
              <v-card-text>#1</v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs4 order-md3 order-xs2>
            <v-card dark tile flat color="red lighten-2">
              <v-card-text>#2</v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs4 order-md1 order-xs3>
            <v-card dark tile flat color="red darken-1">
              <v-card-text>#3</v-card-text>
            </v-card>
          </v-flex>
        </v-layout>
        <v-layout row wrap>
          <v-flex xs12 sm6 md3 order-md4 order-sm2>
            <v-card dark tile flat color="red darken-2">
              <v-card-text>#1</v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm6 md3 order-md3 order-sm1>
            <v-card dark tile flat color="deep-orange lighten-1">
              <v-card-text>#2</v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm6 md3 order-md2 order-sm4>
            <v-card dark tile flat color="deep-orange darken-3">
              <v-card-text>#3</v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm6 md3 order-md1 order-sm3>
            <v-card dark tile flat color="deep-orange">
              <v-card-text>#4</v-card-text>
            </v-card>
          </v-flex>
        </v-layout> -->
      </v-container>   
    </v-app>
  </v-card> 
</template>

<script>
import Experiencia from './Experiencia';
import Proyectos from './Proyectos';
  export default {
    name: 'HelloWorld',
    components: {    
    Experiencia,
    Proyectos
  },

    data: () => ({
    modulosMto:['Modulo repuestos','Modulo Proveedores',
    'Modulo Costos','Modulo Mantenimiento','Modulo Informes'] 
    }),
  }
</script>

<style scoped>
.name{
  color:white;
  background-color: #434E5E;
 
   
}
.contacto{
background-color:#F64D08;/*#F68308 */
color: white;/*#D7DBDD */
}
 
   .cardPrincipal{
     box-shadow: 0 0 0 2em #F4AAB9,
              0 0 0 4em #66CCFF;
      margin: 4em;
      padding:1em;
   }
   img{
     
   }
   

</style>