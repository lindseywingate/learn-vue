<template>
    <div v-bind:id="background-color">
	<p>{{ productName }}</p>	
    </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    productName: String
  }
}
</script>

<style scoped>
.card {
    background: red; 
    border: 1px solid black;
}
</style>
