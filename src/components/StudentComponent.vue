<script setup>
// defineProps(['studentName', 'studentAge', 'studentGrade', 'studentLocation'])

import {inject} from 'vue'
const studentName = inject('studentName')
const studentAge = inject('studentAge')
const studentGrade = inject('studentGrade')
const studentLocation = inject('studentLocation')
</script>

<template>
  <h1>Name:{{ studentName }}</h1>
  <h1>Age:{{ studentAge }}</h1>
  <h1>Grade:{{ studentGrade }}</h1>
  <h1>Location:{{ studentLocation }}</h1>
</template>
