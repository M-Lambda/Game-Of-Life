<template>
  <div class='controls'>
    <span>
      <a-button-group>
        <a-button 
          type="primary"
          :disabled="mainComponent !== 'gamePage'"
          :title="!isRunning ? 'Play' : 'Pause'"
          @click="send('play')"
        > 
          <a-icon  :type="!isRunning ? 'caret-right' : 'pause'"/>
        </a-button>
        <a-button 
          type="primary"
          title="Next Step"
          @click="send('nextStep')"
        > 
          <a-icon type="step-forward" /> 
        </a-button>
      </a-button-group>
    </span>
    <span>
      <a-button-group>
        <a-button
          type="primary"
          title="Decrease Speed"
          @click="send('slowDown')"
        >
          <a-icon type="fast-backward" /> 
        </a-button>
        <a-button
          type="primary"
          title="Increase Speed"
          @click="send('speedUp')"
        >
          <a-icon type="fast-forward" /> 
        </a-button>
      </a-button-group>
    </span>
    <span>
      <a-button-group>
        <a-button
          type="primary"
          title="Clear"
          @click="send('redoSession')"
        >
          <a-icon type="border-inner" /> 
        </a-button>
        <a-button
          type="primary"
          title="Random"
          @click="send('randomSeed')"
        >
          <a-icon type="appstore" /> 
        </a-button> 
      </a-button-group>
    </span>
    <span>
      <a-button-group>
          <a-button
            type="primary"
            title="Import"
            @click="send('importSession')">
            <a-icon type="import" />
          </a-button>
          <a-button
            type="primary"
            title="Export"
            @click="send('exportSession')">
            <a-icon type="export" />
          </a-button>
      </a-button-group>
    </span>
  </div>
</template>

<script>
export default {
  props: {
    isRunning: {
      default: false,
      type: Boolean,
    },
    mainComponent: {
      default: "gamePage",
      type: String,
    },
  },
  methods: {
    send: function (event) {
      this.$emit("send", event);
    },
  },
};
</script>

<style>
.controls {
  display: flex;
  justify-content: center;
}
.ant-btn-group{
  margin: 12px;
}
.ant-btn-primary {
  border-color:#000c17 !important;
  background: hsl(209, 63%, 19%);
  border-left-color: #000c17 !important;
}
.ant-btn-primary:hover {
  background:#000c17;
}
.ant-btn-primary:active,
.ant-btn-primary:focus {
  background:hsl(209, 63%, 19%);
}
</style>
