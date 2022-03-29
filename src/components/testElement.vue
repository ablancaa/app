<template>
    <div>
        <h1 v-if="esPar">I am odd</h1>
        <h1 v-else>{{ count }}</h1>
        <span v-if="!esPar" class="esMultiplo">Es múltiplo de 3</span> 
        <br/><br/>
        
          <button class="btn" v-bind:class="[primary ? primaryClass :'', btnNormal]" @click="increaseCount()">click me!</button>
          <h3>Alberto Blanca Alcaddide</h3>
           <h1>{{size}}</h1><p>HOLA</p>
    </div>
    <br/>
</template>

<script>    
    export default {
        name: "testElement",
        components: {},
        props: {
            elements: Number,
            color: String,
            size: Number,
        },
        data(){
            return{
                count: 6,
                values: [
                    { id: 1, name: "AAA" },
                    { id: 2, name: "BBB" },
                ],
            };
        }, methods: {
            increaseCount () {
                
                if((this.size % 3) == 0){
                    this.count+1;
                    this.esPar = false;
                    this.primary = true;
                    console.log(this.count+" Es múltiplo de 3")
                } else {
                    this.esPar= true;
                    this.primary = false;
                    console.log(this.count+" NO es múltiplo de 3")
                }
            },
        },
    }
</script>

<style scoped>
.btn {
    background-color: white;
    width: 150px;
    height: 40px;
    border: 5px solid red;
    border-radius: 12px;
}
.btn--primary {
    border: 5px solid rgb(2, 58, 7);
    background-color: rgb(127, 243, 152);
}
</style>