<template>
    <div>
        v-bind <br/>
        <input 
            v-model="value"
        /> <br/>
        <input 
            v-bind:value="value"
            v-on:input="input"
        /> <br/>
        <input 
            :value="value"
            @input="input"
        /> <br/>
        <span
            :class="[value]"
        > {{value}} </span>
        <span
            :style="{color: value}"
        > {{value}} </span>
    </div>
</template>

<script>
export default {
    name:'lab3',
    data(){
        return{
            value: ''
        }
    },
    methods:{
        input(inpiutEl){
            this.value += inpiutEl.data
        }
    }
}
</script>

<style scoped>
.red{
    background-color: red;
}
.green{
    background-color: green;
}
.yellow{
    background-color: yellow;
}
.blue{
    background-color: blue;
}
</style>