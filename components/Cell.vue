<template>
  <div
    :class="isAlive.isAlive ? 'alive' : 'dead'"
    class="cell"
    @click="reborn(true)"
    @mouseover="reborn(isMouseDown)"/>
</template>
<script>
export default {
  props: {
    statusObj: {
      default: function () {
        return { isAlive: false };
      },
      type: Object,
    },
    xPos: {
      default: -1,
      type: Number,
    },
    yPos: {
      default: -1,
      type: Number,
    },
    isMouseDown: {
      default: false,
      type: Boolean,
    },
  },
  data() {
    return {
      isAlive: this.statusObj,
    };
  },
  methods: {
    reborn: function (bool) {
      if (bool) {
        this.isAlive.isAlive = !this.isAlive.isAlive;
        this.$emit("wasUpdated", this.isAlive.isAlive);
      }
    },
  },
};
</script>

<style>
.cell {
  flex: 1;
  border-right: 1px solid #001529;
  border-bottom: 1px solid #001529;
  padding-bottom: 100%;
}
.alive {
  background-color: hsl(209, 63%, 19%);
}
.cell:hover {
  background-color: hsl(209, 63%, 19%);
}
.alive:hover {
  background-color:#001529;
}
</style>