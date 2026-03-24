<script setup>
import { ref } from 'vue';

const hasError = ref(true)
const changeClass = () => {
  hasError.value = !hasError.value
}
</script>

<template>
<button
  class="button" :class="{'has-error': hasError}"
>
  Active
</button>

<button @click="changeClass">{{hasError ? "Remove class" : "Add class"}}</button>
</template>

<style scoped>
.button {
  width: 100px;
  height: 30px;
  border-radius: 5px;
  background-color: rgb(80, 9, 146);
  color: white;
  cursor: pointer;
  &:hover{
    background-color:  rgb(121, 7, 227);
  }
}

.has-error {
  background-color: rgb(149, 4, 4);
  &:hover{
    background-color:  rgb(233, 8, 8);
  }
}
</style>
