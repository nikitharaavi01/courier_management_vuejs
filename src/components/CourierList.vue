<script setup>
import CourierItem from './CourierItem.vue';
    defineProps(['couriersData'])
</script>

<template>
  <div class="container">
    <table id="couriers_table">
      <thead>
        <th>Cons No</th>
        <th>Entry Date</th>
        <th>Parcel Type</th>
        <th>Source</th>
        <th>Destination</th>
        <th>Status</th>
        <th>Actions</th>
      </thead>
    <tbody>
      <tr v-for='courier in couriersData'>
        <CourierItem :courier="courier" />
      </tr>
    </tbody>
</table>
  </div>
</template>
<style scoped>
.container {
margin-top: 20px;
}
#couriers_table {
  font-family: Arial, Helvetica, sans-serif;
  border-collapse: collapse;
  margin: 15px 10px;
  width: 90%;
  margin: auto;
}

#couriers_table td, #couriers_table th {
  border: 1px solid #ddd;
  padding: 8px;
}

#couriers_table tr:nth-child(even){background-color: #f2f2f2;}

#couriers_table tr:hover {background-color: #ddd;}

#couriers_table th {
  padding-top: 12px;
  padding-bottom: 12px;
  text-align: left;
  background-color: darkslategray;
  color: white;
}
.view_btn {
    border: none;
    padding: 10px 20px;
    background-color: #2f8263;
  color: white;
  border-radius: 5px;
  cursor: pointer;
}
.courier-item {
  display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
</style>