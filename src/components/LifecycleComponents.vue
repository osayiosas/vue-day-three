<script setup>
import { ref, onBeforeMount, onMounted, onBeforeUpdate, onUpdated, onBeforeUnmount } from 'vue'
const message = ref('hello world')

//lifecycle methods

onBeforeMount(() => {
  console.log('Before Mount')
})

onMounted(() => {
  console.log('Mounted')
})

onBeforeUpdate(() => {
  console.log('Before Update')
})

const updatemessage = () => {
  message.value = 'Hello Vue 3'
}

onUpdated(() => {
  console.log('Updated')
})
onBeforeMount(() => {
  console.log('Before Mount')
})
onBeforeUnmount(() => {
  console.log('Before Unmount')
})
</script>

<template>
  <p>{{ message }}</p>
  <button @click="updatemessage">Update Message</button>
</template>
