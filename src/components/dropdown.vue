<template>
<div>
  <div class="dropdown">
      <button class="dropbtn">choose a day</button>
      <!-- {{days}} -->
      {{days}}
      <select v-if="days.length > 0">
        <option v-for='day in days' :key='day'>{{day.day}}</option>
        <!-- <option value="tue">tuesday</option>
        <option value="wed">wednesday</option>
        <option value="thu">thursday</option>
        <option value="fri">friday</option> -->
      </select>
  {{mensaCount}}
      <!-- <div class="dropdown-content">
        <a href="#">monday</a>
        <a href="#">tuesday</a>
        <a href="#">wednesday</a>
        <a href="#">thursday</a>
        <a href="#">friday</a>
      </div>-->
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
  color: white;
}
</style>