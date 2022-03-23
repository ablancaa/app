<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/FotoPerfil.jpg" height="150">
   <testElement :size="count" />
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
  data(){}
}
</script>



















