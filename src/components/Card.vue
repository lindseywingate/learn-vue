<template>
    <div class="card">
      <p>Thanksgiving Dinner</p>
      <p>{{ currentDate }}</p>
      <p v-for="item in food" :key="item.name">{{item.course}}. {{item.name}}</p>
    </div>
</template>

<script>
var moment = require('moment');
export default {
  name: 'Card',
  methods: {
  },
  computed: {
    currentDate() {
      return moment().format("MMM Do YYYY");
    },
  },
  data() {
    return {
      food: [
        {name: 'apple salad', course: 1},
        {name: 'rice pilaf', course: 2},
        {name: 'turkey', course: 3},
        {name: 'pie', course: 4},
      ],
    }
  },
};
</script>

<style scoped>
.card {
    background: #D6EAF8; 
    border: 1px solid #5DADE2;
}
</style>
