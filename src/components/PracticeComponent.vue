<script setup>
import { inject } from 'vue'

const friendsList = inject('friends')
const gamesList = inject('games')
const moreGamesList = inject('moreGames')
</script>

<template>
  <h4>Injecting Arrays</h4>
  <ul v-for="(friends, index) in friendsList" :key="index">
    <li>
      {{ friends }}
    </li>
  </ul>

  <hr />

  <h4>injecting object!</h4>

  <ul v-for="(games, index) in gamesList" :key="index">
    <li>
      {{ games }}
    </li>
  </ul>

  <hr />

  <h4>injecting array of objects!</h4>

  <ul v-for="(moreGames, index) in moreGamesList" :key="index">
    <li>
      {{ moreGames }}
    </li>
  </ul>

  <hr />

  <h4>objects destructuring!</h4>

  <ul v-for="({ name, genre, platform, releaseDate, location, teamSize }, index) in moreGamesList" :key="index">
    <li>
      {{ name }}
    </li>
    <li>
      {{ genre }}
    </li>
    <li>
      {{ platform }}
    </li>
    <li>
      {{ releaseDate }}
    </li>
    <li>
      {{ location }}
    </li>
    <li>
      {{ teamSize }}
    </li>
  </ul>
</template>
