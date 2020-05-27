<template>
<div>
  <table class="table">

    <th id="cat1">category</th>
    <th>day</th>
    <th id="nam1">name</th>
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
  padding-left: 1vw;
}

#cat1 {
  padding-right: 5vw;
  padding-left: 0vw;
}
#nam1 {
  padding-left: 20vw;
  /* text-align: center; */
}
</style>