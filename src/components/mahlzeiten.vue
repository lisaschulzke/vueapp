<template>
      <li>
          <h5>{{meals.category}}</h5>
          <h4>{{meals.day}}</h4>
          <h4>{{meals.name}}</h4>
      </li>
</template>

<script>
export default {
  name: 'mahlzeiten',
  props: {
    meals: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
li {
  margin-top: 5vh;
  margin-left: auto;
  margin-right: auto;
}
</style>