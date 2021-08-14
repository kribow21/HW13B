<template>
    <main>
        <button v-on:click="toggleStyle">Click for Alternate View</button>
        <div v-bind:class="{gridContainer: isContainer }">
            <TweetInfo v-for="info in tweet" 
            v-bind:key="info.id" 
            :user="info.userVar"
            :post="info.postVar"
            :datePosted="info.datePosted"
            ></TweetInfo>
        </div>
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
                        isContainer : false,
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
                    {
                        userVar : "@kristinb24",
                        postVar : "This is my fourth tweet!",
                        datePosted : "11-08-24",
                        id : 4
                    }

                ]
                
        }
        },
        methods : {
            toggleStyle : function(){
                console.log("You clicked");
                if (this.isContainer == true){
                    this.isContainer = false
                }else if(this.isContainer == false){
                    this.isContainer = true
                }
            }
            }
    }   
</script>

<style scoped>
.gridContainer{
    display: grid;
    grid-template-columns: 1fr 1fr;
}
</style>