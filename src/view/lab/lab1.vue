<template>
    <div>
        v-model <br/>
        <input v-model="value"/> <br/>
        {{value}} <br/>
        <input 
            v-bind:value="value"
            v-on:input="input"
        /> <br/>
    </div>
</template>

<script>
export default {
    name:'lab1',
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