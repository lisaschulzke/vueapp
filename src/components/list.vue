<template>
<div>
  <table class="table">
      <tr>
        <th>monday</th>
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
    msg: String,
    loadedData: String,
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