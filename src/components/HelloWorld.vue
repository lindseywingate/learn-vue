<template>
  <div>
    <p v-for="item in purchases" :key="item.customerName">
      <Card v-bind:customer="{
        customerName: item.customerName, 
        customerStreet: item.customerStreet, 
        customerCity: item.customerCity, 
        customerStateProvince: item.customerStateProvince, 
        customerZip: item.customerZip
        }"></Card>
    </p>
  </div>
</template>

<script>
var moment = require('moment');
import Card from './Card.vue'
export default {
  name: 'HelloWorld',
    computed: {
    currentDate() {
      return moment().format("MMM Do YYYY");
    },
  },
  components: {
    Card
  },
  data() {
    return {
      purchases: [
        {
          customerName: "Frank", 
          customerStreet: "123 Test Street",
          customerCity: "Roseville",
          customerStateProvince: "California",
          customerZip: "95661",
          items: [
            {name: 'apple salad', course: 1},
            {name: 'rice pilaf', course: 2},
            {name: 'turkey', course: 3},
            {name: 'pie', course: 4},
          ]
        },
        {
          customerName: "Bob", 
          customerStreet: "123 Diamond Lane",
          customerCity: "Roseville",
          customerStateProvince: "California",
          customerZip: "95661",
          items: [
            {name: 'caesar salad', course: 1},
            {name: 'risotto', course: 2},
            {name: 'turkey', course: 3},
            {name: 'pie', course: 4},
          ]
        }
      ],
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
