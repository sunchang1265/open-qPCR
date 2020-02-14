<template>
  <!-- template must be wrapped by a tag (div,p etc...) at the very top level -->
  <div class="stage">
    <div>{{ stageData.name + ' - ' + stageData.type}}</div>
    <div v-for="step in stageData.steps" :key="step.name">
        <Step :stepData="step"/>
    </div>
  </div>
</template>

<script>
import Step from './Step.vue'

export default {
  name: 'Stage',
  props: {
    stageData: Object
  },
  components: {
      Step
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.stage {
    border: 1px solid black;
    width: 10vw;
    height: 44vh;
}
</style>
