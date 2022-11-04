

<template>
  <div class="home">
    <h1>Home</h1>
    <h2>{{myTitle}}</h2>
<h1>{{counterData.title}}:</h1>
    <div>
      <button @click="dicreaseValue" class="btn">-</button>
      <button class="counter">{{counterData.count}}</button>
      <button @click="increaseValue" class="btn">+</button>
    </div>


    <div class="edit">
      <h1>Edit the Title:</h1>
      <input v-model="counterData.title" type="text"/>
    </div>
  </div>
</template>

<script setup>
import { reactive } from "vue"

const myTitle = 'My excilent Counter!'

// const counter = ref(0),
// counterTitle = ref('My Counter')

const counterData = reactive({
  count: 0,
  title: 'My Counter'
})

    const increaseValue = () =>{
      counterData.count++
    }
    const dicreaseValue = () =>{
      counterData.count--
    }

</script>


<style >
.home{
  text-align: center;
  padding: 2px;
}
.btn,.counter{
  font-size: 40px;
  margin: 10px;

}
.edit{
  margin-top: 20px;
}
</style>
