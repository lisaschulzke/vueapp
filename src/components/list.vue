<template>
<div>
  <table class="table">
      <!-- <tr v-if="meals.length > 0">
        <th>monday</th>
        <! <td v-for='meal in meals' :key='meal'>{{meals.meal}}</td> -->
        <!-- <td>meal 2</td>
        <td>meal 2</td>
      </tr> -->
      <tr v-if='days.length > 0'>
        <th v-for='day in days' :key="day">{{days.day}}</th>
        <td>meal 1</td>
        <td>meal 2</td>
      </tr>
      <tr>
        <th>tuesday</th>
        <td>meal 1</td>
        <td>meal 2</td>
      </tr>
      <tr>
        <th>wednesday</th>
        <td>meal 1</td>
        <td>meal 2</td>
      </tr>
      <tr>
        <th>thursday</th>
        <td>meal 1</td>
        <td>meal 2</td>
      </tr>
      <tr>
        <th>friday</th>
        <td>meal 1</td>
        <td>meal 2</td>
      </tr>
    </table>
    {{loadedData}}
    </div>
</template>

<script>
export default {
  name: "list",
  props: {
    mensaFact: Object,
    loadedData: String,
    meals: Array,
    days: Array
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