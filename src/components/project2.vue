<template>
    
  <v-hover v-slot="{ isHovering, props }"
       open-delay="200">

  </v-hover>
       
   <v-card
       class="mx-auto text-center"
       max-width="400"
       height="400"
       image="@/assets/Screenshot 2024-01-05 at 21.42.23.png"
       @click="overlay = !overlay"
       theme="dark"
       :elevation="isHovering ? 64 : 2"
       :class="{ 'on-hover': isHovering }"
       v-bind="props"

  >
   <v-container class="fill-height align-center justify-center">
       <v-card-title >

       <div class="text-center">
           <h2>"THE LOBSTER"</h2>
       </div>
       
   </v-card-title>
   </v-container>
  
   
 
     
   
  
  </v-card>

   
   <v-spacer/>


  <v-overlay v-model="overlay" class="background"  contained="false">
   <v-container class=" align-center">
       <v-container>
   <v-row>
     <v-col cols="10" offset="2" >
       <v-img
                   :width="1080"
                   aspect-ratio="16/9"
                   cover
                   src="@/assets/Screenshot 2024-01-05 at 21.42.23.png"
                   ></v-img>
           </v-col>
   </v-row>

       <v-row>
     <v-col cols="10" offset="2">
               <h1>"THE LOBSTER" for Bottega Veneta</h1>
               <p>
                The products in this line feature organic and sculptural shapes that evoke a sense of movement and fluidity.
                With a youthful spirit, the pieces are infused
                with vibrant colorsand playful details.
                The overall effect is a surreal and futuristic interpretation of nature, showcasing
                Bottega’s Veneta’s innovative approach to fashion.
                
               </p>
               <v-img :width="1080"
                   aspect-ratio="16/9"
                   cover
                   src="@/assets/Screenshot 2024-01-05 at 21.43.26.png">
                   
               </v-img>
               <p>
                A bench, consisting of five tubes connected through a stainless steel frame
                and softened with sponge for comfort.
                The techniques uesed are firstly leather treatment and
                second of all flocking and velding.
               </p>
           </v-col>
   </v-row>

       <v-row>
           <v-col col="10" offset="2">
               <v-img :width="1080"
                   aspect-ratio="16/9"
                   cover
                   src="@/assets/Screenshot 2024-01-05 at 21.43.12.png">
                   
               </v-img>
               <h2>Renders made with v-ray</h2>
           </v-col>
       </v-row>
          
           
 </v-container>

       
       
       
       
   </v-container>
   
  
  </v-overlay>
</template>

<script >
  


  export default {
    data: () => ({
      overlay: false,
      isHovering: false
    })

   //  watch: {
   //    overlay (val) {
   //      val && setTimeout(() => {
   //        this.overlay = false
   //      }, 2000)
   //    },
    
  }
</script>
<style>
.background{
    background-color: white !important;
    opacity: 1;
}

.v-overlay__scrim {
	background: white;
  position:fixed !important;
  opacity: 1;
}


</style>