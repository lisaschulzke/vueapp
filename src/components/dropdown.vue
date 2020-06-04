<template>
<div>
  <div class="dropdown">
      <select class="select" name="selectbutton">
        <option v-for='day in days' :key='day'>{{day}}</option>
        <!-- <option value="tue">tuesday</option>
        <option value="wed">wednesday</option>
        <option value="thu">thursday</option>
        <option value="fri">friday</option> -->
      </select>
  <!-- {{mensaCount}} -->
    </div>

    </div>
</template>

<script>
export default {
  name: 'dropdown',
  props: {
    mensaCount: Object,
    days: Array,
    title: String,
  },
};
</script>

<style scoped>
.select {
  margin-left: 30px;
  margin-top: 5px;
  cursor: pointer;
  color: black;
}
</style>