<script setup>
import { computed, reactive, ref } from 'vue';
const first_name = ref("Nguyen Khac")
const last_name = ref("Minh")

const full_name = computed({
  get() {
    return first_name.value + ' ' + last_name.value
  },

  set(new_value) {
    [first_name.value, last_name.value] = new_value.split(",")
  }
})

const changeName = () => {
  full_name.value = "Nguyen Van, A"
}
</script>

<template>
<div>
  <h2>Fullname:: {{ full_name }}</h2>
  <h2>Firstname:: {{ first_name }}</h2>
  <h2>Lastname:: {{ last_name }}</h2>

  <button @click="changeName">Change name</button>
</div>
</template>

<style scoped>
</style>
