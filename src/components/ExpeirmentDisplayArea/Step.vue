<template>
  <!-- template must be wrapped by a tag (div,p etc...) at the very top level -->
  <div class="step">
    <div>{{ stepData.name }}</div>  
  </div>
</template>

<script>
export default {
  name: 'step',
  props: {
    stepData: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.step {
    border: 1px solid black;
    padding: 1vw;
}
</style>
