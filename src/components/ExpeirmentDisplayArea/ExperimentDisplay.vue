<template>
  <div class="experiment-display">
    <div v-for="stage in experimentData.stages" :key=stage.name>
      <Stage :stageData="stage" />
    </div>
  </div>
</template>

<script>
import Stage from './Stage.vue'

export default {
  name: 'ExperimentDisplay',
  props: {
    experimentData: Object
  },
  components: {
    Stage
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.experiment-display {
  background-color: orange;
  color: white;   
  height: 44vh;
  padding: 0.5vh 1vw 0.5vh 1vw;
}
</style>
