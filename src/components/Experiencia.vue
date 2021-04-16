 <!--Linea de tiempo Experiencia-->
  <template>
    <v-container class="container" style="max-width: 600px;">
      <v-timeline  dense clipped class="timeline" >
        <v-timeline-item             
          hide-dot>               
            <i class="fas fa-book-open fa-lg"></i><strong class="ml-2 text">ESTUDIOS</strong>
        </v-timeline-item>
        
        <v-timeline-item         
          class="mx-0"           
          color="#434e5e"
          icon-color="grey lighten-2"
          small> 
          <v-layout justify-space-between>       
            <v-flex xs10 class="my-1 text">Colegio Integrado San Pablo - Bachiller</v-flex>
            <v-flex hidden-xs-only md1 text-xs-right class="texto">2005</v-flex>
          </v-layout>             
        </v-timeline-item>

        <v-timeline-item                
          color="#434e5e"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10 class="texto">Tecnólogo en Sistemas Informáticos</v-flex>
            <v-flex hidden-xs-only md1 text-xs-right>2012</v-flex>
          </v-layout>
          <v-flex xs10 class="texto">Universidad de Caldas</v-flex>
        </v-timeline-item>

        <v-timeline-item                
          color="#434e5e"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10 class="text">Tecnólogo en Electrónica</v-flex>
            <v-flex hidden-xs-only md1 text-xs-right class="texto">2016</v-flex>
          </v-layout>
          <v-flex xs10>Universidad de Caldas</v-flex>
        </v-timeline-item>

        <v-timeline-item                
          color="#434e5e"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10 class="texto">                    
              Ingeniería en Informática</v-flex>
            <v-flex  hidden-xs-only sm4 md2 text-xs-right class="texto">2017-2021</v-flex>
          </v-layout>
          <v-flex xs10 class="texto">Universidad de Caldas</v-flex>
        </v-timeline-item>

        <v-timeline-item
          hide-dot
          color="#434e5e">   
          <v-flex>           
              <i class="fas fa-briefcase fa-lg"></i>
            <span class="ml-2 mx-1 texto"><strong>EXPERIENCIA</strong></span>                
          </v-flex>  
        </v-timeline-item>

        <v-timeline-item                      
          color="#434e5e"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10 class="texto">Panadería La Victoria S.A</v-flex>                  
            <v-flex hidden-xs-only sm4 md2 text-xs-right class="texto">2008-2015</v-flex>
          </v-layout>                
        </v-timeline-item>

        <v-timeline-item
          hide-dot>                 
            <p class="text">
              ELECTRÓNICO: Garantizar el óptimo funcionamiento de 
              los equipos tanto en la electrónica, predecir posibles fallas y minimizar los 
              tiempos de paradas no programados, realizar mantenimiento preventivo y documentar las actividades 
              realizadas.
            </p>                                
        </v-timeline-item>

        <v-timeline-item                
          color="#434e5e"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10 class="texto">Panadería La Victoria S.A</v-flex>                  
            <v-flex hidden-xs-only sm4 md2 text-xs-right class="texto">2015-2017</v-flex>
          </v-layout>                
        </v-timeline-item>

        <v-timeline-item
          hide-dot>                 
            <p class="text">
              LIDER MTO: Coordinar y realizar mantenimiento preventivo y 
              correctivo de equipos automatizados en la parte eléctrica, electrónica, programación 
              de dispositivos autónomos “PLC, MICROCONTROLADORES Y VARIADORES” para poder cumplir
              con los estándares de producción.
            </p>                                
        </v-timeline-item>

          <v-timeline-item                
          color="#434e5e"
          icon-color="grey lighten-2"
          small>
            <v-layout justify-space-between>
              <v-flex xs10 class="texto">Panadería La Victoria S.A</v-flex>                  
              <v-flex hidden-xs-only md1 text-xs-right class="texto">2020</v-flex>
            </v-layout>                
        </v-timeline-item>

        <v-timeline-item
          hide-dot>                 
            <p class="text">
              Software de mantenimiento: Aplicativo web desarrollado para el area 
              de mantenimiento, el cual permite llevar un control de todos los equipos de la compañia.              
            </p>     
            <ul>
              <li v-for="item in modulosMto " :key="item" v-text="item" class="texto"></li>                      
            </ul>                           
        </v-timeline-item>          
        <!-- Proyectos -->      
            <Proyectos/>             
        <!-- Fin -->   
        
        <!-- <v-timeline-item 
          fill-dot
          class="white--text mb-5"
          color="purple"
          large>
          <template v-slot:icon>
            <span>JL</span>
          </template>                  
        </v-timeline-item> -->     
      </v-timeline>
    </v-container>
</template>
          <!--Fin Experiencia -->
<script>
import Proyectos from './Proyectos';
  export default {
    name: 'Experiencia',

    components:{
      Proyectos
    },

    data: () => ({
    modulosMto:['Modulo Repuestos','Modulo Proveedores',
    'Modulo Costos','Modulo Mantenimiento','Modulo Informes'] 
    }),
  }
</script>
<style scoped>
.text{
  text-align: justify; 
  margin-right: 15px;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
.texto{
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
.container{
  margin-left: 0;
  padding: 0px 0px 15px 0px;
  align-content: flex-start;
}

.time{
  margin-left: 0;
  padding: 0;
  align-content: flex-start;
  text-align: start;
}
.timeline{
    position: relative;
    min-width: 0px;   
    align-items: left;
    justify-content: left;
    padding: 0px 0px 0px 0px;
}

</style>
