<template>
  <table>
    <thead>
      <tr>
        <th></th>
        <th>Mon</th>
        <th>Tue</th>
        <th>Wed</th>
        <th>Thu</th>
        <th>Fri</th>
        <th>Sat</th>
        <th>Sun</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(label, i) in hours" :key="i">
        <td class="hourlabel">{{ label }}</td>
        <td
          class="timeslot"
          v-for="day in Array(7).keys()"
          :key="day"
          :class="getClass(day, i)"
        >&nbsp;</td>
      </tr>
      <tr>
        <td class="hourlabel">{{ hours[0] }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
import { format } from 'date-fns';

export default {
  methods: {
    getClass(day, hour) {
      if (day <= 4 && hour > 8 && hour < 18) {
        return 'business';
      }
      return 'nightwknd';
    },
  },
  computed: {
    hours() {
      return Array.from(Array(24).keys())
        .map(i => format(new Date().setHours(i), 'h A'));
    },
  },
};
</script>

<style>
  table {
    border-collapse: collapse;
  }
  td.business {
    background-color: lightpink;
  }
  td.nightwknd {
    background-color: aliceblue;
  }
  td.hourlabel {
    position: relative;
    top: -13px;
    font-size: 0.7em;
  }
  td.timeslot {
    border: 1px solid #ddd;
    width: 40px;
    cursor: pointer;
  }
</style>
