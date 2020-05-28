<template>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="50vw"
      img-height="20vh"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd">

      <b-carousel-slide v-for="mealsTable in dataTable" :key="mealsTable"
        img-src="https://picsum.photos/1024/480/?image=52"> 
        <mahlzeiten  :meals="mealsTable"></mahlzeiten>
      </b-carousel-slide>
    </b-carousel>
</template>

<script>
import mahlzeiten from "../components/mahlzeiten.vue";
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
/* ul {
  padding-top: 5vh;
}

#cat1 {
  padding-right: 5vw;
  padding-left: 0vw;
}
#nam1 {
  padding-left: 20vw;
  /* text-align: center; */
/* }
#list {
  padding-top: 30vh;
  margin-top: 30vh;
} */

#carousel-1 {
  width: 10vw;
  height: 50vh;
}
</style>