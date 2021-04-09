<template class="grad">    
  <v-flex>
          <v-timeline-item
          hide-dot
          color="purple">   
          <v-flex>           
              <i class="fas fa-file-code fa-lg"></i>
            <span class="ml-2 mx-1"><strong>PROYECTOS</strong></span>                
          </v-flex>  
        </v-timeline-item>

        <v-timeline-item          
          color="blue"
          small>                           
            <h5 class="ml-2 mx-1">E-COMMERCE</h5>   
            <hr>  
              <v-flex>
            <i class="fab fa-angular fa-lg ml-1" style="color:#BF0011"></i> 
            <i class="fab fa-cuttlefish fa-sm ml-2" style="color:#4B026D"></i><span class="tama"><strong># .Net Core</strong></span>
            <p>Sistema de administracion de ventas y productos.</p>  
          </v-flex>       
        </v-timeline-item> 

        <v-timeline-item          
          color="blue"
          small>                           
            <h5 class="ml-2 mx-1">SOFTWARE MANTENIMIENTO</h5>   
            <hr>  
              <v-flex>
            <i class="fab fa-vuejs fa-lg ml-3" style="color:#1D5201"></i> 
            <i class="fab fa-cuttlefish fa-sm ml-2" style="color:#4B026D"></i><span class="tama"><strong># .Net Core</strong></span>
            <p>Sistema que simplifica y automatiza las operaciones de mantenimiento de la compañia .</p>  
          </v-flex>       
        </v-timeline-item> 
        <v-flex class="ml-8" md8>
          <Carousel/>
        </v-flex>
                
  </v-flex>
</template>

<script>
import Carousel from './Carousel';
export default {
    components:{
      Carousel
    },
    name:'Proyectos',
    
    data:()=>({

    })
}
</script>
<style scoped>
.tama{
  font-size: 13px;
}
</style>
