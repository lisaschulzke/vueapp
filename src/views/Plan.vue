<template>
<div>
  <div class="header" id="navigationbar">
    <h3 class="headline">mensa app</h3>
    <!-- {{loadedData.data}} -->
    <dropdown :days='loadedData.day'></dropdown>
  </div>
  <list :dataTable='loadedData.name' id='tablecontent'>{{mahlzeiten}}</list>
      
</div>
</template>

<script>
import list from '../components/list.vue'
import dropdown from '../components/dropdown.vue'
import axios from 'axios'
// import mahlzeiten from '../components/mahlzeiten.vue'
export default {
  name: "Plan",
  components: {
    list,
    dropdown
  },
  props: {
    
  },
  data: function() {
    return {
      loadedData: 'no data loaded',
    }
  },
  mounted() {
    axios.get('http://3.121.41.235:3000/meals/60')
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
  background-color: grey;
  display: flex;
  flex-direction: row;
  height: 15vh;
  width: 100%;
  margin: 0px;
  margin-top: 6vh;
  padding: 8px;
  padding-top: 2vh;
  padding-left: 5vw;
  padding-bottom: 1vh;
  margin-bottom: 1vh;
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
#tablecontent {
  color: black;
  margin-left: 8vw;
}
</style>