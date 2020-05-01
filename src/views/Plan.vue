<template>
  <div class="header" id="navigationbar">
    <h3 id="headline">mensa app</h3>
    <div class="dropdown">
      <button class="dropbtn">choose a day</button>
      <div class="dropdown-content">
        <a href="#">monday</a>
        <a href="#">tuesday</a>
        <a href="#">wednesday</a>
        <a href="#">thursday</a>
        <a href="#">friday</a>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Plan',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
