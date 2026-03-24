<script setup>
  const text = 'Hello'
  const rawHtml = '<span style="color: blue">This should be red.</span>'
  const button_id = 'button'
  const button_class = 'buttonClass'
  const disableButton = false
  const styleButton = {
    style: {
      color: 'red'
    }
  }

  const sum = (a, b) => a + b
</script>

<template>
  <h1>{{ text + ' world' }}</h1>
  <div v-html="rawHtml"></div>
  <button :id="button_id" :class="button_class" :disabled="disableButton" v-bind="styleButton">{{disableButton? 'Disable' : 'Click here'}}</button>
  <div>
    {{ sum(1, 2) }}
  </div>
</template>

<style scoped>
</style>
