<script setup>
  defineProps({
    position: {
      type: Object,
      required: true
    }
  })
</script>

<template>
  <div>
    <h2> {{ position.pos }} </h2>
  </div>
</template>

<style>

</style>