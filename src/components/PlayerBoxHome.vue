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
      <img v-bind:src="'../src/assets/images/' + player.thumbnail" /> 
      <div>
        <h4> {{ player.name }}</h4>
        <h6> {{ player.position }} - {{ player.team }}</h6>

      </div>
      <div>
        <h4 class="player-points"> {{ player.points }}</h4>
      </div>
    </div>

</template>

<style scoped>
.player-box {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: space-between;
}
.player-points {
  display: flex;
  flex-direction: row;
  align-items:center;
}

img {
  border-radius: 20%;
  height: 50px;
}
</style>