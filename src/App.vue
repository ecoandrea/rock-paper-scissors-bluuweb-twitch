<script setup>
import {useGame} from '@/composables/useGame.js'

import GameHeader from "@/components/GameHeader.vue";
import GameOption from "./components/GameOption.vue";
import GameResult from "./components/GameResult.vue";

const {userOption} = useGame()

</script>

<template>
  <main class="text-center mx-auto px-4">
    <GameHeader />
    <GameOption v-if="!userOption" />
    <GameResult v-if="userOption" />
  </main>
</template>
