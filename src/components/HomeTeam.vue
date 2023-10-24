<script setup>
defineProps({
  team: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="home-team-column">

    <span>{{ team.name }} {{ team.position }} {{ team.team }} {{ team.points }}</span>
    
  </div>
</template>

<style scoped>
.home-team-column {
  padding: 20px;
  border: 0.5px solid black;
}
</style>
