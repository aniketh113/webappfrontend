<template>
  <div class="container">
    <HeaderTop TopicName="Top Destinations for Vacation In USA" />
    <PlaceName :places="places" />
  </div>
</template>

<script>
import HeaderTop from './components/HeaderTop.vue'
import PlaceName from './components/PlaceName.vue'
export default {

  name: 'App',
  components: {
    HeaderTop,
    PlaceName
  },
  data() {
    return {
      places: []
    }
  },
  methods: {
    async fetchBooks() {
      const res = await fetch("https://yelgondaaniketh.onrender.com/api")
      const data = await res.json()
      console.log(data)
      return data[0].places;
    }

  },
  async created() {
    this.places = await this.fetchBooks()
  }

}

</script>


<style >
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}


body {
  font-family: "Montserrat", sans-serif;
}

.container {
 
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.4em solid black;
  padding: 30px;
  border-radius: 5px;
  color: rgb(255, 0, 0);
  background-color: rgb(255, 250, 158);
  font-size: 15px;
  max-width:900px;
  border-radius: 30px;
}
</style>