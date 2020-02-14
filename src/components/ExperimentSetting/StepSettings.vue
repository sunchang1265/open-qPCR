<template>
  <!-- template must be wrapped by a tag (div,p etc...) at the very top level -->
  <div class="step-setting">
    <div>{{ StepName }}</div>
    
  </div>
</template>

<script>
export default {
  name: 'StepSetting',
  props: {
    StepName: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.step-setting {
  background-color: lightgrey;  
  height: 44vh;
  padding: 0.5vh 1vw 0.5vh 1vw;
}
</style>
