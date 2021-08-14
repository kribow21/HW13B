<template>
    <div>
    <h3>{{user}}</h3>
    <h4>{{post}}</h4>
    <p>{{datePosted}}</p>
    </div>
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
div{
    border: blueviolet solid 2px;
    margin-bottom: 3%;
    width: 80%;
    padding: 2px;
}

</style>