<script setup>
import { nextTick, reactive, ref } from 'vue';
const count = ref(0)
const obj_info = reactive({
  name: "Minh",
  email: "minhnguyen@gmail.com",
  address: ['Ha Noi', "Thai Binh"]
})


const increase = async () => {
  count.value++
  console.log(document.querySelector("#h1").innerText)
  await nextTick()
  console.log(document.querySelector("#h1").innerText)
}

const addAddress = () => {
  obj_info.address.push("Ninh Binh")
}
</script>

<template>
  <h1 id="h1">{{ count }}</h1>
  <button v-on:click="increase">Increase</button>
  <!-- <button @click="increase">Increase</button> -->

  <h1>Infor User</h1>
  <p>name:: {{ obj_info.name }}</p>
  <p>email:: {{ obj_info.email }}</p>
  <p>address:: {{ obj_info.address }}</p>

  <button @click="addAddress">add address</button>
</template>

<style scoped>
</style>
