<template>
    <div>
        <h1> {{ TopicName }} </h1>
    </div>
</template>

<script>
export default {
    name: 'HeaderTop',
    props: {
        TopicName: String,
    }
}
</script>

<style  scoped>
div {
    text-align: center;
}
</style>