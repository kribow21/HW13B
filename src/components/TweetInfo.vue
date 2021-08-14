<template>
    <ul>
    <li>{{user}}</li>
    <li>{{post}}</li>
    <li>{{datePosted}}</li>
    </ul>
</template>

<script>
    export default {
        name : 'TweetInfo',
        props : {
            user : String,
            post : String,
            datePosted : String
        }
    }
</script>

<style scoped>


</style>