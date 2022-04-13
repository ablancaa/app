<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/FotoPerfil.jpg" height="150">
   <testElement :size="count" />
     </div>
     <div>
      <a @click="url">Click here!</a>
   </div>
   <p>
     {{name()}}
   </p>
   <p>{{lastName()}}</p>


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
      name: "John",
      lastName: "Doe",
      url:"https://www.uoc.edu",
    }
  },
  computed:{
    fullName(){
		return this.name +' '+ this.lastName;
  },
  watch: {
  name(name) {
    this.name = name;
  },
  lastName(lastName) {
    this.lastName = lastName;
  }
}


  }
}
</script>



















