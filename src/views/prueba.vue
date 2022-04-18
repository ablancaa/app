<template>
    <div>
<h1>Prueba</h1>
       <div>
           <input type="text" v-model="name"/>
           <input type="text" v-model="lastName"/>
      
<p>{{name}}</p>

<p>{{lastName}}</p>

<p>{{fullName}}</p>
  </div>
    </div>
</template>

<script>
    export default {
        name: 'Prueba-1',
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
}
    }
</script>

<style lang="scss" scoped>

</style>