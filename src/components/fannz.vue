<template>
    
  <v-hover v-slot="{ isHovering, props }"
       open-delay="200">

  </v-hover>
       
   <v-card
       class="mx-auto text-center"
       max-width="400"
       height="400"
       image="@/assets/416354135_416858847347606_6319937310102119339_n.jpg"
       @click="overlay = !overlay"
       theme="dark"
       :elevation="isHovering ? 64 : 2"
       :class="{ 'on-hover': isHovering }"
       v-bind="props"

  >
   <v-container class="fill-height align-center justify-center">
       <v-card-title >

       <div class="text-center">
           <h2>ABOUT ME</h2>
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
                   src="@/assets/416354135_416858847347606_6319937310102119339_n.jpg"
                   ></v-img>
           </v-col>
   </v-row>

       <v-row>
     <v-col cols="10" offset="2">
               <h1>About me</h1>
               <p>
                Hi, I’m Fannar. A 27 year old Designer from Iceland that studied in IED Milano.

With a passion for creating spaces that blend functionality and aesthetics, I thrive on transforming ordinary places into extraordinary experiences. Inspired by Iceland's unique nature, my designs often reflect a harmonious blend of modern aesthetics and the raw beauty of my homeland.

               </p>

               
               


              
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