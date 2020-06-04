<template>
<div>
  <b-card
    title="Card Title"
    img-src="https://picsum.photos/600/300/?image=25"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2">
    <b-card-text>
      
      Some quick example text to build on the card title and make up the bulk of the card's content.
    </b-card-text>
    <mahlzeiten  :meals="mealsTable">{{mahlzeiten}}</mahlzeiten>
    <mahlzeiten v-for='mealsFromTable in dataTable' :key='mealsFromTable'></mahlzeiten>
    <!-- <b-button href="#" variant="primary" class="buttonVote">upvote</b-button> -->
    <!-- <b-button href="#" variant="primary" class="buttonVote">downvote</b-button> -->
    <button v-on:click="sendUpvote(data.id)"><b-icon icon="hand-thumbs-up" variant="success"></b-icon> (0)</button>
    <button v-on:click="sendDownvote(data.id)"><b-icon icon="hand-thumbs-down" variant="danger"></b-icon> (0)</button>
  </b-card>
</div>
</template>

<script>
import mahlzeiten from "../components/mahlzeiten.vue";
import axios from 'axios'

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
  },
  methods: {
    sendUpvote: function(likedID) {
      console.log("sending upvote for " + likedID);
      axios.post("http://3.121.41.235:3000/meals/60", {
        id: likedID
      }).then((res) => {
        console.log("Result: " + res)
      }).catch((error) =>{
        console.log("Could not POST:" + error);
      });
      },
    sendDownvote: function(likedID) {
      console.log("Sending downvote for " + likedID)
      }
    }
};
</script>

<style scoped>
.buttonVote{
  margin: 1rem;
}
</style>