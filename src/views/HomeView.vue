

<template>
  <div class="home">
    <h1>Home</h1>

    <div>
      <button @click="dicreaseValue" class="btn">-</button>
      <button class="counter">{{counter}}</button>
      <button @click="increaseValue" class="btn">+</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue"

const counter = ref(0)

    const increaseValue = () =>{
      counter.value ++
    }
    const dicreaseValue = () =>{
      counter.value--
    }

</script>

<!----
<script>
import { ref } from "vue"
export default ({
  setup() {
    const counter = ref(0)

    const increaseValue = () =>{
      counter.value ++
    }
    const dicreaseValue = () =>{
      counter.value--
    }


    return{
    counter,
    increaseValue,
    dicreaseValue
  }
  },

 
})
</script>

--->
<!-----
<script>


export default ({
  data() {
    return{
      counter: 0,
    }
  },
  methods:{
increaseValue(){
  this.counter ++
},
dicreaseValue(){
  this.counter --
}
  }
})
</script>
---->

<style >
.home{
  text-align: center;
  padding: 2px;
}
.btn,.counter{
  font-size: 40px;
  margin: 10px;

}
</style>
