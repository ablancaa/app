<template>
    <div>
        <h1 v-if="esPar">I am odd</h1>
        <h1 v-else>{{count}}</h1>
        <br/><br/>
          <button class="btn" @click="increaseCount(size)">click me!</button>
          
    </div>
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
                esPar: true,
                count: 6,
                size: 1,
                values: [
                    { id: 1, name: "AAA" },
                    { id: 2, name: "BBB" },
                ],
            };
        }, methods: {
            increaseCount: function () {
                this.count=this.count+this.size;
                if((this.count % 3) == 0){
                    this.count+1;
                    this.esPar = false;
                    console.log(this.count+" Es múltiplo de 3")
                } else {
                    this.esPar= true;
                    console.log(this.count+" NO es múltiplo de 3")
                }
            },
        },
    }
</script>

<style lang="scss" scoped>

</style>