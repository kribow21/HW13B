<template>
    <main>
    <button v-on:click="toggleStyle">Click for Alternate View</button>
    <TweetInfo v-bind:class="{ grid : isGrid, list : isList}" v-for="info in tweet" 
    v-bind:key="info.id" 
    :user="info.userVar"
    :post="info.postVar"
    :datePosted="info.datePosted"
    ></TweetInfo>
    </main>
</template>

<script>
import TweetInfo from './TweetInfo.vue'
    export default {
        name : 'TweetCollection',
        components : {
            TweetInfo
        },
                data : function (){
            return {
                        isList : true,
                        isGrid : false,
                tweet : [
                    {
                        userVar : "@kristinb21",
                        postVar : "This is my first tweet!",
                        datePosted : "11-08-21",
                        id : 1
                    },
                    {
                        userVar : "@kristinb22",
                        postVar : "This is my second tweet!",
                        datePosted : "11-08-22",
                        id : 2
                    },
                    {
                        userVar : "@kristinb23",
                        postVar : "This is my third tweet!",
                        datePosted : "11-08-23",
                        id : 3
                    },

                ]
                
        }
        },
        methods : {
            toggleStyle : function(){
                console.log("You clicked");
                        this.isList = false
                        this.isGrid = true
            }
            }
    }   
</script>

<style scoped>
.grid{
    display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    border: 2px rgb(226, 43, 171) solid; 
    height: 100px;
    list-style: none;
    align-content: center;

}
.list{
    border: 2px blueviolet solid; 
    margin-bottom: 5%;
    width: 600px;
}
</style>