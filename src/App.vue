<template>
  <div id="app">
    <WeeklySchedule style="float: left"/>
    <div class="schedules">
      <h2>Schedules</h2>
      <p><span class="swatch blue">&nbsp;</span> Nights/weekends</p>
      <p><span class="swatch pink">&nbsp;</span> Business hours</p>
      <p><button>Add schedule</button></p>
      <p></p>
      <p>Select a schedule and then click and drag to apply that schedule to hours of the week.</p>
    </div>
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
.schedules {
  float: left;
  padding: 30px;
  text-align: left;
}
.swatch {
  width: 20px;
  height: 20px;
  border: 1px solid #ddd;
  display: inline-block;
}
.blue {
  background-color: aliceblue;
}
.pink {
  background-color: lightpink;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
