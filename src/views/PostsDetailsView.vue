
<template>
  <div class="about">
    <h1>PostsDetails</h1>
    <p> this is the content of the {{$route.params.id}}</p>
    <div>
      <button @click="showPostId">Show ID</button>
    </div>
    <div>
      <button @click="goHomein3sec">GoHome3Sec</button>
    </div>
    <div>
      <button @click="goFirstPage">GoFirstPage</button>
    </div>

    <p><RouterLink to="/posts">&lt; Back</RouterLink></p>
  </div>
</template>
<script setup>
import {vAutofocus} from '@/Derictive/vAutofocus'
import {useRoute, useRouter} from 'vue-router'

const routee = useRoute()
const router = useRouter()


const showPostId = ()=>{
  alert(`This the the Post of ID: ${routee.params.id}`)
}

// const goHomein3sec =()=>{
// setTimeout(()=>{
// router.push('/')
// },3000)
// }


const goHomein3sec =()=>{
setTimeout(()=>{
router.push({ name: 'home'})
},3000)
}
const goFirstPage =()=>{
setTimeout(()=>{
router.push({ 
  name: 'postsDetails',
  params:{
    id: 'id1'
  }

})
})
}
</script>

