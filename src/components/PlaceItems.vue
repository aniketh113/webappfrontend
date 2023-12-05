<template>
    <div>
        <h2>{{ place.title }}</h2>
        <h4>Season to Visit: {{ place.season_to_visit }} </h4>
        <h4>History: {{ place.history }}</h4>
        <h4>Things to Do: {{ place.things_to_do }}</h4>
        <h4>Airport Distance: {{ place.distance_from_airport }} miles</h4>
        <h4>Food: {{ place.food }}</h4>
    </div>
</template>

<script>
export default {
    name: 'PlaceItems',
    props: {
        place: Array
    }
}
</script>

<style scoped>
h1 {
    border: 3px solid black;
    background-color: rgb(221, 242, 242);
}
h2{
    text-align: center;
}
div {
    
    background-color: white;
    color: black;
    padding: 1em;
    margin: 5px;
    font-weight: bold;
    font-size: 15px;
}
</style>
