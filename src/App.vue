<script setup>
import { ref } from 'vue';

  const isShow = ref(true)
  const handleHidden = () => {
    isShow.value = !isShow.value
  }
</script>

<template>
<h1 v-if="isShow">Hello</h1>
<h1 v-else>Hi</h1>

<h1 v-show="false">Check v-show</h1>
<button @click="handleHidden">{{isShow ? "Hidden" : "Show"}}</button>
</template>

<style scoped>
</style>
