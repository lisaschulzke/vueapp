<template>
<div>
  <div class="header" id="navigationbar">
    <h3 class="headline">mensa app</h3>
    <div class="dropdown">
      <!-- <button class="dropbtn">choose a day</button> -->
      <select class="select" name="selectbutton">
        <option value="0">select day</option>
        <option value="mon">monday</option>
        <option value="tue">tuesday</option>
        <option value="wed">wednesday</option>
        <option value="thu">thursday</option>
        <option value="fri">friday</option>
      </select>
      <!-- <div class="dropdown-content">
        <a href="#">monday</a>
        <a href="#">tuesday</a>
        <a href="#">wednesday</a>
        <a href="#">thursday</a>
        <a href="#">friday</a>
      </div>-->
    </div>
  </div>
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
    </div>

</template>

<script>
export default {
  name: "Plan",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  color: whitesmoke;
  background-color: black;
  display: flex;
  flex-direction: row;
  height: 15vh;
  width: 100%;
  margin: 0px;
  margin-top: 6vh;
  padding: 8px;
  padding-top: 2vh;
  padding-left: 5vw;
}
.select {
  margin-left: 30px;
  margin-top: 5px;
  cursor: pointer;
  color: white;
}

.headline {
  margin-top: 0px;
}

.table {
  text-align: left;
  margin-top: 10vh;
  margin-left: 0px;
  color: black;
}
th,
td {
  padding-left: 5vw;
}
</style>
