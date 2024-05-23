<script setup>
import { ref, watch } from 'vue'

const location = ref('Hello World')
const inputText = ref('')

//watch for changes

watch(inputText, (newValue, oldValue) => {
    console.log('New Value:', newValue)
    console.log('Old Value:', oldValue)
  location.value = `You typed: ${newValue}`
})
</script>

<template>
   <div>
    <h1>{{ location }}</h1>
    <input v-model="inputText" placeholder="type something" >
   </div>
</template>