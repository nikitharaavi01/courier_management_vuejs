<script setup>
    defineProps(['courier'])
</script>
<template>
      <td>{{ courier.Consignmentnumber }}</td>
      <td>{{ courier.Entrydatetime }}</td>
      <td>{{ courier.Parceltype }}</td>
      <td>{{ courier.Source }}</td>
      <td>{{ courier.Destination }}</td>
      <td>{{ courier.Status }}</td>
      <td>
          <button class="view_btn">View</button>
      </td>
</template>
<style scoped>
    h1 {
        text-align: center;
        margin: 10px 0;
    }
#couriers_table {
  font-family: Arial, Helvetica, sans-serif;
  border-collapse: collapse;
}

#couriers_table td, #couriers_table th {
  border: 1px solid #000;
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
</style>