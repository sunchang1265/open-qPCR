<template>
  <div id="app"> 
    <!-- if bind varable data, using v-bind, shorthand is ":", e.g. Header, Experiment-Display-->
    <!-- if just passing  primitive values, directly call the props name, e.g. Footer-->
    <Header v-bind:experimentName="experiment.name"/>
    <Experiment-Display :experimentData="experiment"/>
    <Step-Setting StepName="Current Step"/>
    <Footer experimentStatus="Not stated" />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import ExperimentDisplay from './components/ExpeirmentDisplayArea/ExperimentDisplay.vue'
import StepSetting from './components/ExperimentSetting/StepSettings.vue'

var experiment = {
  name: "experiment1",
  stages: [
    {
      name: "stage1",
      type: "holding",
      steps: [
        { name: "step1"}
      ]
    }
  ] 
}

export default {
  name: 'App',
  components: {
    Header,    
    Footer,
    ExperimentDisplay,
    StepSetting
  },
  data(){
    return {
      experiment: experiment
    }
  }
}
</script>

<style>
html, body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  position: relative;
}
</style>
