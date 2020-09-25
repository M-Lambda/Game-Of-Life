<template>
  <div class='stats'>
    <span>Cell Count: {{ cellCount }}</span>
    <span>Speed: {{ currentSpeed }}</span>
    <br/>
    <br/>
    <span>{{ currentGeneration }} Generations</span>
    <span>{{ cellsCreated }} Births</span>
    <span>{{ cellsAlive }} Alive</span>
    <span>{{ cellsDeath }} Death</span>
  </div>
</template>


<script>
export default {
  props: {
    currentGeneration: {
      default: 0,
      type: Number,
    },
    cellCount: {
      default: 0,
      type: Number,
    },
    cellsAlive: {
      default: 0,
      type: Number,
    },
    cellsDeath: {
      default: 0,
      type: Number,
    },
    cellsCreated: {
      default: 0,
      type: Number,
    },
    currentSpeed: {
      default: 0,
      type: Number,
    },
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scoped>
.stats{
  margin-bottom: 24px;
  text-align:center;
}
span{
  margin: 12px;
  color: hsl(209, 63%, 19%);
}
</style>
