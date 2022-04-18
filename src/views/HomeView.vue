<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/FotoPerfil.jpg" height="150">
   <testElement :size=25 />
     </div>
     <div>
      <a v-bind:href="url" target="_blank">Click here!</a>
   </div>


</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import testElement from "@/components/testElement.vue";
export default {
  name: 'HomeView',
  components: {
    testElement,
  }, 
  data(){
    return{
      size: 25,
      url:"https://www.uoc.edu" 
    }
  }
}
</script>



















