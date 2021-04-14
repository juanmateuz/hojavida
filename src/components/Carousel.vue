<template>
  <v-layout row>  <!-- open card -->   
    <v-row class="margin justify-start mb-3 font">
      <v-col>
        <v-dialog transition="dialog-bottom-transition" max-width="700">
          <template v-slot:activator="{ on, attrs }">
            <v-btn class="mr-7" small outlined color="teal" v-bind="attrs" v-on="on">Open Proyect
            </v-btn>
          </template>

          <template v-slot:default="dialog">
            <v-card>
              <v-toolbar color="secondary" dark class="font">Software Mantenimiento</v-toolbar>
              <!-- <v-card-text>
                <div class="text-h2 pa-12">Hello world!</div>
              </v-card-text> -->             
              <v-carousel hide-delimiters width="400" height="auto" class="carousel">
                <v-carousel-item class="img" v-for="(item,i) in items" :key="i"                              
                  reverse-transition="fade-transition">      
                    <div id="div1" class="d-flex flex-column justify-space-between align-center" >   
                        <v-img :src="item.src" class="img"></v-img>                        
                    </div>               
                </v-carousel-item>
              </v-carousel>            
              <!-- -->
              <v-card-actions class="justify-end">
                <v-btn text @click="dialog.value = false">Cerrar</v-btn>
              </v-card-actions>
              <!-- -->
            </v-card>
          </template>
        </v-dialog>
      </v-col>  
    </v-row>       
  </v-layout>
</template>



<script>
export default {
  name:'Carousel',
  data:()=>({
    items: [
          {
            src: require('../assets/Mto/software.jpg'),
          },
          {
            src:  require('../assets/Mto/diag.jpg'),
          },
          {
            src:  require('../assets/Mto/software3.jpg'),
          },
          {
            src: require('../assets/Mto/soft.jpg'),
          },
        ],
  })
}
</script>

<style scoped>
.margin{
  margin-top: 0;
  margin: 0px 0px 0px 100px;  
}
.font{
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
.img{
  width: 100%;
  max-width: 700px;
  height: auto; 
}
.carousel{
   width:"200px";
   height:"200px"
}
</style>