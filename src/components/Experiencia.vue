 <!--Linea de tiempo Experiencia-->
  <template>
    <v-container style="max-width: 600px;">
      <v-timeline dense clipped>
        <v-timeline-item                
          hide-dot>
          <v-flex>         
            <i class="fas fa-book-open fa-lg"></i><strong class="ml-2">ESTUDIOS</strong>
          </v-flex >                
        </v-timeline-item>
        
        <v-timeline-item                
          color="purple"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10>Colegio Integrado San Pablo - Bachiller</v-flex>
            <v-flex hidden-xs-only md1 text-xs-right>2005</v-flex>
          </v-layout>                
        </v-timeline-item>

        <v-timeline-item                
          color="purple"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10>Tecnólogo en Sistemas Informáticos</v-flex>
            <v-flex hidden-xs-only md1 text-xs-right>2012</v-flex>
          </v-layout>
          <v-flex xs10>Universidad de Caldas</v-flex>
        </v-timeline-item>

        <v-timeline-item                
          color="purple"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10>Tecnólogo en Electrónica</v-flex>
            <v-flex hidden-xs-only md1 text-xs-right>2016</v-flex>
          </v-layout>
          <v-flex xs10>Universidad de Caldas</v-flex>
        </v-timeline-item>

        <v-timeline-item                
          color="purple"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10>                    
              Ingeniería en Informática</v-flex>
            <v-flex  hidden-xs-only sm4 md2 text-xs-right>2017-2021</v-flex>
          </v-layout>
          <v-flex xs10>Universidad de Caldas</v-flex>
        </v-timeline-item>

        <v-timeline-item
          hide-dot
          color="purple">   
          <v-flex>           
              <i class="fas fa-briefcase fa-lg"></i>
            <span class="ml-2 mx-1"><strong>EXPERIENCIA</strong></span>                
          </v-flex>  
        </v-timeline-item>

        <v-timeline-item                      
          color="green"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10>Panadería La Victoria S.A</v-flex>                  
            <v-flex hidden-xs-only sm4 md2 text-xs-right>2008-2015</v-flex>
          </v-layout>                
        </v-timeline-item>

        <v-timeline-item
          hide-dot>                 
            <p>
              ELECTRÓNICO MANTENIMIENTO: Garantizar el óptimo funcionamiento de 
              los equipos tanto en la electrónica, predecir posibles fallas y minimizar los 
              tiempos de paradas no programados, realizar mantenimiento preventivo y documentar las actividades 
              realizadas.
            </p>                                
        </v-timeline-item>

        <v-timeline-item                
          color="green"
          icon-color="grey lighten-2"
          small>
          <v-layout justify-space-between>
            <v-flex xs10>Panadería La Victoria S.A</v-flex>                  
            <v-flex hidden-xs-only sm4 md2 text-xs-right>2015-2017</v-flex>
          </v-layout>                
        </v-timeline-item>

        <v-timeline-item
          hide-dot>                 
            <p>
              LIDER MTO: Coordinar y realizar mantenimiento preventivo y 
              correctivo de equipos automatizados en la parte eléctrica, electrónica, programación 
              de dispositivos autónomos “PLC, MICROCONTROLADORES Y VARIADORES” para poder cumplir
              con los estándares de producción.
            </p>                                
        </v-timeline-item>

          <v-timeline-item                
          color="green"
          icon-color="grey lighten-2"
          small>
            <v-layout justify-space-between>
              <v-flex xs10>Panadería La Victoria S.A</v-flex>                  
              <v-flex hidden-xs-only md1 text-xs-right>2020</v-flex>
            </v-layout>                
        </v-timeline-item>

        <v-timeline-item
          hide-dot>                 
            <p>
              Software de mantenimiento: Aplicativo web desarrollado para el area 
              de mantenimiento, el cual permite llevar un control de todos los equipos de la compañia.              
            </p>     
            <ul>
              <li v-for="item in modulosMto " :key="item" v-text="item"></li>                      
            </ul>                           
        </v-timeline-item>          
        <!-- Proyectos -->        
          <main>
            <Proyectos/>
          </main>       
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
