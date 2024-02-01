<template>
    
   <v-hover v-slot="{ isHovering, props }"
        open-delay="200">

   </v-hover>
        
    <v-card
        class="mx-auto text-center"
        max-width="400"
        height="400"
        image="@/assets/01_Bar_View_(1)-transformed (1).jpeg"
        @click="overlay = !overlay"
        theme="dark"
        :elevation="isHovering ? 64 : 2"
        :class="{ 'on-hover': isHovering }"
        v-bind="props"

   >
    <v-container class="fill-height align-center justify-center">
        <v-card-title >

        <div class="text-center">
            <h2>RESTAURANT</h2>
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
                    src="@/assets/01_Bar_View_(1)-transformed (1).jpeg"
                    ></v-img>
            </v-col>
		</v-row>

        <v-row>
			<v-col cols="10" offset="2">
                <h1>Restaurant in an unknown place</h1>
                <p>
                    During the conceptualization and design of
                    the restaurant,
                    I aimed to create a truly inviting and unique dining experience.
                    The ambiance is defined by a harmonious blend
                    of carefully selected materials and
                    an abundance of natural lighting, fostering a bright yet cozy atmosphere that resonates with warmth.
                    One of the distinctive features of the establishment lies in the fact that
                    I personally conceptualized and rendered
                    all the furniture.
                    This approach not only allows for a cohesive and well-thought-out design but also ensures
                    that each piece is a testament to the attention to detail that went into crafting the overall aesthetic.
                </p>
                <v-img :width="1080"
                    aspect-ratio="16/9"
                    cover
                    src="@/assets/04.Reception (1).jpg">
                    
                </v-img>
                <p>
                    The utilization of premium materials not only adds an element of sophistication
                    but also contributesto the establishment’s overall visual appeal.
                    The natural lighting, strategically incorporated, plays a pivotal role in creating
                    an uplifting and vibrant environment, making it an ideal setting for users to enjoy
                    their dining experience.
                    In essence, the restaurant is a testament
                    to my commitment to create spaces that not only meet functional requirements
                    but also elevate the overall sensory experience.
                    I believe that the design, with its unique blend of bright aesthetics
                    and cozy elements, sets the stage for a memorable and delightful experience for the user.
                </p>
            </v-col>
		</v-row>

        <v-row>
            <v-col col="10" offset="2">
                <v-img :width="1080"
                    aspect-ratio="16/9"
                    cover
                    src="@/assets/03.Sitting (1).jpg">
                    
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