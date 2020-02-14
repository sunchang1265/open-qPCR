<template>
  <!-- template must be wrapped by a tag (div,p etc...) at the very top level -->
  <div class="header-bar">
    <div>{{ experimentName }}</div>
    
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    experimentName: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header-bar {
  background-color: black;
  color: white; 
  /* including padding will be 5vh in total */ 
  height: 4vh;
  line-height: 4vh;
  padding: 0.5vh 1vw 0.5vh 1vw;
}
</style>
