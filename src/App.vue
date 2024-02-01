<template>

	<v-container>
		<v-row>
			<v-col cols="6">
				<Project1/>
			</v-col>
			<v-col cols="6">
				<Project2/>
			</v-col>
			
			
		</v-row>
		<v-row>
			<v-col cols="6">
				<Project3/>
			</v-col>
			<v-col cols="6">
				<Project4/>
			</v-col>
		</v-row>
		<v-row>
			<v-col cols="6" offset="3">
				<fannar/>
			</v-col>
			
		</v-row>
	</v-container>
 
 
</template>

<script >
  import Project1 from './components/project1.vue'
  import Project2 from './components/project2.vue'
  import Project3 from './components/project3.vue'
  import Project4 from './components/project4.vue'
  import fannar from './components/fannz.vue'


  export default {
    components:{
      Project1,
	 Project2,
	 Project3,
	 Project4,
	 fannar
    },
    data: () => ({
      overlay: false,
    }),

    watch: {
      overlay (val) {
        val && setTimeout(() => {
          this.overlay = false
        }, 2000)
      },
    },
  }
</script>

<style>

</style>