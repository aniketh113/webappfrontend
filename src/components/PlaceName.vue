<template>
    <div class="SiteNames">
        <div v-for="place in places" :key="place.id">
            <PlaceItems :place="place" />
        </div>
    </div>
</template>

<script>
import PlaceItems from './PlaceItems.vue'
export default {
    name: 'PlaceName',
    components: {
        PlaceItems
    },
    props: {
        places: Array
    }
}
</script>


<style scoped>
.SiteNames {
    background-color: rgb(179, 154, 255);
    padding: 1em;
    max-width: 100%;
    height: auto;
    margin-top:30px;
}
</style>
