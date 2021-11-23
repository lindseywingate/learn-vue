<template>
    <div class="card">
      <p>Thanksgiving Dinner</p>
      <a v-on:click="log">Log Food</a>
      <ul id="foodList">
        <li v-for="item in food" :key="item.name">{{item.name}}</li>
      </ul>
    </div>
</template>

<script>

export default {
  name: 'Card',
  methods: {
    log() {
    },
  },
  computed: {
    currentDate() {
      return Date.now();
    }
  },
  data() {
    return {
      food: [
        {name: 'turkey', course: 3},
        {name: 'apple salad', course: 1},
        {name: 'rice pilaf', course: 2}
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
