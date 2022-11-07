
<template>
  <div class="about">
    <h1>Posts</h1>
    <textarea v-autofocus/>
  </div>
  <ul>
    <li><RouterLink to="/postsDetails/id1">Post1</RouterLink></li>
    <li><RouterLink to="/postsDetails/id2">post2</RouterLink></li>
    <li><RouterLink to="/postsDetails/id3">post3</RouterLink></li>
  </ul>
</template>

<script setup>
import {vAutofocus} from '@/Derictive/vAutofocus'
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

