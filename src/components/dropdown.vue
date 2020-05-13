<template>
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
</template>

<script>
export default {
  name: "dropdown",
  props: {
    msg: String,
    loadedData: String,
  },
};
</script>

<style scoped>
.select {
  margin-left: 30px;
  margin-top: 5px;
  cursor: pointer;
  color: white;
}
</style>