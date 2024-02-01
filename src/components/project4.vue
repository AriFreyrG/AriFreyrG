<template>
    
  <v-hover v-slot="{ isHovering, props }"
       open-delay="200">

  </v-hover>
       
   <v-card
       class="mx-auto text-center"
       max-width="400"
       height="400"
       image="@/assets/30_Billboard_Mockup_Templates_for_Outdoor_Advertising-transformed.png"
       @click="overlay = !overlay"
       theme="dark"
       :elevation="isHovering ? 64 : 2"
       :class="{ 'on-hover': isHovering }"
       v-bind="props"

  >
   <v-container class="fill-height align-center justify-center">
       <v-card-title >

       <div class="text-center">
           <h2>MARKETING</h2>
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
                   src="@/assets/30_Billboard_Mockup_Templates_for_Outdoor_Advertising-transformed.png"
                   ></v-img>
           </v-col>
   </v-row>

       <v-row>
     <v-col cols="10" offset="2">
               <h1>Campaign for Verti Italy</h1>
               <p>
                An assignment for Verti.
Given the hashtag #conVERTIti.
The aim was to modernize and find new design and interactive ways
for costumers to enjoy the benefits of Verti. While focusing on three
main values, Aquire, Engage & Maintain.
A youtful and playful take on a the very black and white business that insurances are.

               </p>


               <v-img :width="1080"
                   aspect-ratio="16/9"
                   cover
                   src="@/assets/Untitled design (8) (1).png">
                   
               </v-img>


               <p>
                In our opinion the interaction between a company and consumer should be
transperant and an open line of communication while building trust in eachother.
Interactive billboard, will allow costumers to acces
a website in which
they can send in insurance related confeesion in a way that makes Verti a friend.
By using both humor and relatability Verti showcases understanding of the clients
everyday experiences and a part of their daily life.
Camera Billboard, will have and built in camera, that captures the targetas they walk by.
Allowing costumer to feel as brand ambassadors.
The Verting machine will sell products that are related to protection
and will help the costumer in feeling safe, therefor creating a memorable
as well as an engaging experience for both existing and potential costumers.
               </p>
           </v-col>
   </v-row>

       <v-row>
           <v-col col="10" offset="2">
               <v-img :width="1080"
                   aspect-ratio="16/9"
                   cover
                   src="@/assets/VERTINGMACHINE.png">
                   
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