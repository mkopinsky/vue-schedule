<template>
  <div id="app">
    <WeeklySchedule />
  </div>
</template>

<script>
import WeeklySchedule from './components/WeeklySchedule.vue';

export default {
  name: 'app',
  components: {
    WeeklySchedule,
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
