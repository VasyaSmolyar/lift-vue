<script setup>
defineProps({
  floorCount: {
    type: Number,
    required: true
  },

  selectedFloor: {
    type: Number,
    required: true
  },

  setFloor: {
    type: Function,
    required: true
  }
})
</script>

<template>
  <main>
    <li v-for="(item, index) in Array(floorCount)">
      <input name="floor" type="radio" :checked="selectedFloor === index + 1" v-on:click="setFloor" />  
    </li>
  </main>
</template>