<script setup>
import PlayerBoxAway from './PlayerBoxAway.vue';

defineProps({
  player: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="away-team-column">
    <PlayerBoxAway :player="player"/>
  </div>
</template>
  

<style scoped>
.away-team-column {
  padding: 20px;
  border: 0.5px solid gray;
}
img {
  border-radius: 30%;
  width: 65px;
}
</style>
