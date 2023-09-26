<template>
 <div>
  <Navbar/>
  <div class="steps-block">
    <MultiSteps />
  </div>
</div>
</template>

<script>
import MultiSteps from './components/MultiSteps.vue';
import Navbar from './components/Navbar.vue';

export default {
  name: 'App',
  components: {
    MultiSteps,
    Navbar
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.steps-block {
  margin: 30px 20px;
}
.steps-block input[type=text],
.steps-block input[type=date],
.steps-block input[type=textarea] {
  width: 100%;
}
</style>
