<script setup>
import { reactive, watch} from 'vue'

const state = reactive({useername: 'Osayi'})


//here we cant provide specific properties of obeject
// - we need to provide the whole object, otherwise its gonna give us erorr in console.

watch( 

    () => state.useername, (newValue, oldValue) => {
    console.log('New Value:', newValue)
    console.log('Old Value:', oldValue)
    }
)
</script>

<template>
   <h1>{{ state.useername }}</h1>
   <button @click="state.useername = 'Osaigbovo'">Change Name</button>
</template>