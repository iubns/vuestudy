<template>
  <div>
    <button @click="() => selectedLab = 'lab1'">lab1</button>
    <button @click="() => selectedLab = 'lab2'">lab2</button>
    <button @click="() => selectedLab = 'lab3'">lab3</button>
    <lab-1 v-if="selectedLab === 'lab1'"/>
    <lab-2 v-if="selectedLab === 'lab2'"/>
    <lab-3 v-if="selectedLab === 'lab3'"/>
  </div>
</template>

<script>
import lab1 from './view/lab/lab1.vue'
import lab2 from './view/lab/lab2.vue'
import lab3 from './view/lab/lab3.vue'

export default {
  name: 'App',
  components: {
    lab1,
    lab2,
    lab3,
  },
  data(){
    return{
      selectedLab : 'lab1'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
