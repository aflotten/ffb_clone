<script setup>
import PlayerBox from './PlayerBox.vue';

defineProps({
  player: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="home-team-column">

  <PlayerBox :player="player"/>    
  </div>
</template>

<style scoped>
.home-team-column {
  padding: 20px;
  border: 0.5px solid black;
}
</style>
