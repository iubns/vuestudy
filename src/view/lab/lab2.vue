<template>
    <div>
        v-if & v-show <br/>
        <input type="checkbox" v-model="vIf" /> {{vIf}}
        <input type="checkbox" v-model="vShow" />{{vShow}}
        <div v-for="(value, index) of count"
            :key="'if'+index">
            <span
                v-if="vIf"
            > v-if의 {{index}} 번째 줄입니다.</span>
        </div>
        <div v-for="(value, index) of count"
            :key="'show'+index">
            <span
                v-show="vShow"
            > v-show의 {{index}} 번째 줄입니다.</span>
        </div>
    </div>
</template>

<script>
export default {
    name:'lab2',
    data(){
        return{
            count: new Array(50000),
            vIf: false,
            vShow: false
        }
    }
}
</script>

<style scoped>
    .tempStyle{
        background-color: green
    }
</style>