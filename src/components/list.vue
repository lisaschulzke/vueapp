<template>
<div>
  <table class="table">

    <th>category</th>
    <th>name</th>
    <th>day</th>
    
    </table>
    <mahlzeiten v-for="mealsTable in dataTable" :key="mealsTable" :meals='mealsTable'></mahlzeiten>
    <!-- {{loadedData}} -->
    </div>
</template>

<script>
import mahlzeiten from '../components/mahlzeiten.vue'
export default {
  name: "list",
  props: {
    mensaFact: Object,
    loadedData: String,
    meals: Array,
    days: Array,
    dataTable: String
  },
  components: {
  mahlzeiten
  }
};
</script>

<style scoped>
.table {
  text-align: left;
  margin-top: 20vh;
  margin-left: 0px;
  color: black;
}
th,
td {
  padding-left: 5vw;
}
</style>