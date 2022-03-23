<template>
    <div>
        <h1 v-if="esPar">I am odd</h1>
        <h1 v-else>{{ count }}</h1>
        <span v-if="!esPar" class="esMultiplo">Es múltiplo de 3</span> 
        <br/><br/>
          <button v-bind:class="[primary ? primaryClass :'', btnNormal]" @click="increaseCount()">click me!</button>
          <h3>Alberto Blanca Alcaide</h3>
    </div>
    <br/>
</template>

<script>    
    export default {
        name: "testElement",
        elements: Number,
        color: String,
        components: {},
        props: {},
        data(){
            return{
                primaryClass: 'btn--primary',
                btnNormal: 'btn',
                esPar: true,
                primary: false,
                count: 6,
                size: 1,
                values: [
                    { id: 1, name: "AAA" },
                    { id: 2, name: "BBB" },
                ],
            };
        }, methods: {
            increaseCount () {
                
                this.count=this.count+this.size;
                if((this.count % 3) == 0){
                    //this.count+1;
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
.esMultiplo {
    size: 10px;
}

.btn {
    background-color: white;
    width: 150px;
    height: 40px;
    border: 5px solid red;
    border-radius: 25px;
}

.btn--primary{
    border: 5px solid rgb(2, 58, 7);
    background-color: rgb(127, 243, 152);
}
</style>