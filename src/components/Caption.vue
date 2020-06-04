<template>
    <div class="caption">
        <h1>Anything, anytime, <br>anywhere. We get it.</h1>
        <p>Eiusmod cupidatat anim ullamco amet est.Eiusmod cupidatat anim ullamco amet est.</p>
        <SearchStory />
    </div>
</template>

<script>
import SearchStory from './SearchStory.vue'

export default {
    name: "Caption",
    components: {
        SearchStory
    }
}
</script>

<style lang="scss" scoped>
.caption{
    width:50%;
    margin: auto;
    margin-top: 50px;
    text-align: center;
    h1{
        font-weight: bold;
        font-size:50px;
    }
    p{
        font-size:14px;
        font-weight: 500;
        color:#757575;
        padding: 10px 71px;
    }
     @media  only screen and (max-width:320px){
        width:95%;
        margin-top: 80px;
        h1{
            font-size:27px;
        }
        p{
            padding:10px 20px;
        }
    }
    @media  only screen and (min-width:321px) and (max-width:540px){
        width:95%;
        margin-top: 80px;
        h1{
            font-size:30px;
        }
         p{
            padding:10px 20px;
        }
    }
     @media  only screen and (min-width:541px) and (max-width:720px){
        width:80%;
        margin-top: 80px;
        h1{
            font-size:35px;
        }
         p{
            padding:10px 30px;
        }
         

    }
}

</style>