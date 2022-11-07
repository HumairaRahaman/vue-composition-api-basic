<template>
  <div class="modals">
    <h1>Modals</h1>
    <button @click="showModal = true">Show Modal</button>
    <teleport to=".modals-container">
      <div v-if="showModal" class="modal">
        <h1>This is my modal.</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quam, sunt?</p>
        <button @click="showModal = false">Hide Modal</button>
      </div>
    </teleport>
  </div>
</template>
<script setup>
import { ref } from "vue";

const showModal = ref(false);
</script>

<style scoped>
.modal {
  background: beige;
  padding: 10px;
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: 1;
}
</style>
