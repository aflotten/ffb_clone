<script setup>
defineProps({
  player: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="away-team-column">
    <img v-bind:src="player.thumbnail">
    <span> {{ player.position }} {{ player.name }} {{ player.team }} {{ player.points }}</span>
    
  </div>
</template>
  

<style scoped>
.away-team-column {
  padding: 20px;
  border: 0.5px solid black;
}
img {
  border-radius: 30%;
  width: 65px;
}
</style>
