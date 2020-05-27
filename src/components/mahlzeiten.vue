<template>
      <tr>
          <th>{{meals.category}}</th>
          <td>{{meals.day}}</td>
          <td>{{meals.name}}</td>
      </tr>
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
</style>