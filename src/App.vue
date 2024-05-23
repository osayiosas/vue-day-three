<script setup>
import SchoolComponent from './components/SchoolComponent.vue'
import { provide } from 'vue'

provide('studentName', 'Joanna')
provide('studentAge', 20)
provide('studentGrade', 'A')
provide('studentLocation', ['Lagos', 'Nigeria'])

// const studentName = 'joan'
// const studentAge = 20
// const studentGrade = 'A'
// const studentLocation = 'lagos'

import PracticeComponentVue from './components/PracticeComponent.vue'

//provide Arrays

provide('friends', ['osayi', 'joan', 'ola', 'osaigbovo'])

//provide Objects

provide('games', {
  id: 1,
  name: 'Fifa 22',
  price: 2000,
  genre: ['Sports', 'Football', 'Soccer'],
  platform: ['PS4', 'PS5', 'Xbox'],
  releaseDate: '2021-10-01',
  location: {
    country: 'Nigeria',
    city: 'Lagos',
    street: 'Ikorodu Road'
  },
  teamSize: 12
})

//provide Arrays of objects 

provide('moreGames', [
  {
    id: 1,
    name: 'Fifa 22',
    price: 2000,
    genre: ['Sports', 'Football', 'Soccer'],
    platform: ['PS4', 'PS5', 'Xbox'],
    releaseDate: '2021-10-01',
    location: {
      country: 'Nigeria',
      city: 'Edo',
      street: 'Benin city',
    },
    teamSize: 12
  },
  {
    id: 2,
    name: 'Call of Duty',
    price: 3000,
    genre: ['Action', 'Shooting'],
    platform: ['PS4', 'PS5', 'Xbox'],
    releaseDate: '2023-10-01',
    location: {
      country: 'Nigeria',
      city: 'Lagos',
      street: 'Agbara'
    },
    teamSize: 14
  },
  {
    id: 3,
    name: 'Mortal Kombat',
    price: 2500,
    genre: ['Action', 'Fighting'],
    platform: ['PS4', 'PS5', 'Xbox'],
    releaseDate: '2021-10-01',
    location: {
      country: 'Nigeria',
      city: 'Lagos',
      street: 'Ikeja'
    },
    teamSize: 30
  },
  {
    id: 4,
    name: 'Need for Speed',
    price: 1500,
    genre: ['Racing'],
    platform: ['PS4', 'PS5', 'Xbox'],
    releaseDate: '2024-10-01',
    location: {
      country: 'Nigeria',
      city: 'Lagos',
      street: 'Victoria Island'
    },
    teamSize: 45
  }

])
import {ref} from 'vue'
import LifecycleComponents from './components/LifecycleComponents.vue'

const showHide = ref(true)


import BaiscComponent from './components/BaiscComponent.vue'

import ReactiveObject from './components/ReactiveObject.vue'

</script>

<template>
  <!-- <SchoolComponent :studentName="studentName" :studentAge="studentAge" :studentGrade="studentGrade" :studentLocation="studentLocation" /> -->

  <SchoolComponent />

  <hr />

  <PracticeComponentVue />
  <hr>
  <LifecycleComponents v-if="showHide"/>
  <button @click="showHide = !showHide">Show/Hide</button>

  <hr>
  <BaiscComponent />
  <hr>
  <ReactiveObject />
</template>
