<template>
  <div class="q-pa-md">
     <q-carousel 
        v-model="slide"               
        infinite  
        animated              
        padding                  
        class="shadow-1 rounded-borders"
        ref="carousel"
      >
        <template v-slot:control>    

          <q-carousel-control
            position="bottom-right"
            :offset="[18, 18]"
            class="q-gutter-sm"
          >
            <q-btn
              color="white"
              text-color="black"
              icon="arrow_left"              
              @click="$refs.carousel.previous()"
            />
            <q-btn
              color="white"
              text-color="black" icon="arrow_right"
              @click="$refs.carousel.next()"
            />
          </q-carousel-control>
        </template>        

        <q-carousel-slide          
          class="column no-wrap flex-start q-gutter-sm"
          :name="index"
          v-for="(item, index) in items" :key="item.id">          

          <q-input 
            dense 
            filled
            square            
            outlined             
            :value="item.expression"
          />

          <q-input             
            filled          
            square 
            outlined               
            rows="13"
            type="textarea"               
            :value="item.meaning"            
          />
        </q-carousel-slide>  

      </q-carousel>    
  </div>
</template>

<script>


export default {
  name: 'Carousel',  
  data () {
    return {
      slide: 1,
      items: [
        {
          id: 0,
          expression: 'Hello',
          meaning: 'Used to greet someone'
        },
        {
          id: 1,
          expression: 'Kat',
          meaning: 'Een sort deer'
        }
      ]
    }
  } 
}
</script>

<style>

</style>
