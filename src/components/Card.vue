<template>
<div class="card">
    <div class="personDetails">
      <p><b>{{ customer.customerName }}</b></p>
      <p>{{ customer.customerStreet }}</p>
      <p>{{ customer.customerCity }}, {{ customer.customerStateProvince }}, {{ customer.customerZip }}</p>
    </div>
    <div class="itemDetails">
      <p>test</p>
    </div>
    <div class="shippingDetails">
      <p>shipping details</p>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    customer: Object,
  },
};
</script>

<style scoped>
.card {
    background: #D6EAF8; 
    border: 1px solid #5DADE2;
    display: table;
    width: 100%;
    table-layout: fixed;
    border-spacing: 10px;
}
.personDetails {
  text-align: left;
  display: table-cell;
}
.itemDetails {
  display: table-cell;
  background-color: "red";
}
.shippingDetails {
  display: table-cell;
}
</style>
