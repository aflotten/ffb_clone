<script setup>
defineProps({
  team: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="away-team-column">
    <span> {{ team.image }} {{ team.name }} {{ team.position }} {{ team.team }} {{ team.points }}</span>
    
  </div>
</template>

<style scoped>
.away-team-column {
  padding: 20px;
  border: 0.5px solid black;
}
</style>
