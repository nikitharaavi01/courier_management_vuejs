<script setup>
import { ref , onMounted} from 'vue';
import CourierList from './components/CourierList.vue';
import Navbar from './components/Navbar.vue';

let couriersData = ref([]);

onMounted(() => {
  fetch('https://courier-management-nodejs.onrender.com/api')
    .then(response => response.json())
    .then(res => couriersData.value = res)
})
</script>

<template>
  <header>
    <Navbar />
  </header>

  <main>
    <CourierList :couriersData="couriersData" />
  </main>
</template>

<style scoped>

</style>
