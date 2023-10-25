<script setup>
import PlayerBoxHome from './PlayerBoxHome.vue';

defineProps({
  player: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="home-team-column">

  <PlayerBoxHome :player="player"/>    
  </div>
</template>

<style scoped>
/* .home-team-column {
  padding: 20px;
  border: 0.5px solid gray;
} */
</style>
