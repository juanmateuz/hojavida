<template>
  <v-flex  md8>
    <v-carousel
    cycle
    height="300">
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"      
        reverse-transition="fade-transition"
        transition="fade-transition"
      ></v-carousel-item>
    </v-carousel>
  </v-flex>  
</template>
<script>
export default {
  name:'Carousel',
  data:()=>({
    items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
  })
}
</script>