<script setup>
defineProps({
  player: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="player-box">
    <h4> {{ player.name }}</h4>
    <h6> {{ player.position }}</h6>
    <h6> {{ player.team }}</h6>
    <h6> {{ player.points }}</h6>
  </div>

</template>

<style scoped>
.player-box {
  display: flex;
  flex-direction: column;
}
</style>