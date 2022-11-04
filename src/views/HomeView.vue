

<template>
  <div class="home">
    <h1>Home</h1>
    <h2>{{myTitle}}</h2>
<h1>{{counterData.title}}:</h1>
    <div>
      <button @click="dicreaseValue(2)" class="btn">--</button>
      <button @click="dicreaseValue(1)" class="btn">-</button>
      <button class="counter">{{counterData.count}}</button>
      <button @click="increaseValue(1)" class="btn">+</button>
      <button @click="increaseValue(2)" class="btn">++</button>
    </div>
<p>This is the {{computedValue}} number</p>

    <div class="edit">
      <h1>Edit the Title:</h1>
      <input v-model="counterData.title" type="text"/>
    </div>
  </div>
</template>

<script setup>
import { computed, reactive, watch } from "vue"

const myTitle = 'My excilent Counter!'

const computedValue = computed(()=>{
if(counterData.count % 2 === 0) return 'even'
return 'odd'
})



const counterData = reactive({
  count: 0,
  title: 'My Counter'
})

watch(()=> counterData.count,(newCount)=>{
  if(counterData.count == 20)
alert('This is pretty, you may go home now!!!')
})
    const increaseValue = amount =>{
      counterData.count+= amount
    }
    const dicreaseValue = amount =>{
      counterData.count-=amount
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
