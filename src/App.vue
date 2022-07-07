<script setup>
import Elevator from './components/Elevator.vue';
import { ELEVATORS_COUNT, FLOORS_COUNT } from './constants';
import Floors from './components/Floors.vue';
</script>

<script>
export default {
  data() {
    return {
      elevatorsFloor: Array(ELEVATORS_COUNT).fill(1),
      floor: 1
    }
  },

  methods: {
    setFloor: (index) => floor = index,
  },

}
</script>

<template>
  <main>
    <li v-for="(item, index) in elevatorsFloor">
      <Elevator :floors="FLOORS_COUNT" :floor=item />
    </li>
    <Floors :set-floor="setFloor" :floor-count="FLOORS_COUNT" :selected-floor="floor" />
  </main>
</template>
