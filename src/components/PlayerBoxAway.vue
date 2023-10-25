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
      <div >
        <h6> {{ player.points }}</h6>
      </div>
      <h6> {{ player.team }}</h6>
      <h6> {{ player.position }}</h6>
      <h4> {{ player.name }}</h4>
      <img v-bind:src="'../src/assets/images/' + player.thumbnail" /> 
    </div>

</template>

<style scoped>
.player-box {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

img {
  border-radius: 20%;
  height: 50px;
}
</style>