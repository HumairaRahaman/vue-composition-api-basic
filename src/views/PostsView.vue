
<template>
  <div class="about">
    <h1>Posts</h1>
    <textarea v-autofocus/>
  </div>
  <ul>
    <li v-for="post in posts"
    :key="post.id"
    ><RouterLink :to="`/postsDetails/${post.id}`">{{post.title}}</RouterLink></li>
    
  </ul>
</template>

<script setup>
import {vAutofocus} from '@/Derictive/vAutofocus'
import { ref } from 'vue';


const posts = ref([
  {
id: 'id1',
title: 'post1'
},
{
id: 'id2',
title: 'post2'
},
{
id: 'id3',
title: 'post3'
},

])
</script>
<style scoped>
ul{
  margin-top: 20px;
}
li{
  text-decoration: none;
  font-style: none;
  list-style: none;
}
</style>

