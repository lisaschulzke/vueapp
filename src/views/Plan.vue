<template>
<div>
  <div class="header" id="navigationbar">
    <h3 class="headline">mensa app</h3>
    <dropdown></dropdown>
    {{loadedData}}
    <list></list>   
  </div>
</div>
</template>

<script>
import list from '../components/list.vue'
import dropdown from '../components/dropdown.vue'
import axios from 'axios'

export default {
  name: "Plan",
  components: {
    list,
    dropdown
  },
  props: {
    msg: String
  },
  data: function() {
    return {
      loadedData: 'no data loaded',
    }
  },
  mounted() {
    axios.get('http://localhost:3000/mensa/Di')
    .then(response => {
      this.loadedData = response

    })
    .catch(error => {
      console.log(error);
    })
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
/* .select {
  margin-left: 30px;
  margin-top: 5px;
  cursor: pointer;
  color: white;
} */

.headline {
  margin-top: 0px;
}

/* .table {
  text-align: left;
  margin-top: 10vh;
  margin-left: 0px;
  color: black;
}
th,
td {
  padding-left: 5vw;
} */
</style>
