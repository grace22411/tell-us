<template>
    <div class="search-story">
        <input type="text"  placeholder="Search stories"/>
        <div class="arrow">
            <i class="fas fa-angle-right"></i>
        </div>
    </div>
</template>
<script>
export default {
    name:"SearchStory",
    // data: {
    //     search: ""
    // }
}
</script>

<style lang="scss" scoped>
    .search-story{
        display: flex;
        width:100%;
        justify-content: center;
        align-items: center;
        input{
            height:50px;
            width:55%;
            border:1px solid #CFCFCF;
            background-color: #fff;
            font-family: 'Poppins', sans-serif;
            padding-left:20px;
        }

        .arrow{
            width:7%;
            height: 50px;
            background-color: #045B7E;;
            padding-top:10px;
            i{
                font-size:25px;
                color:#fff;
            }
        }
        @media  only screen and (max-width:320px){
            input{
                width:70%;
            }
            .arrow{
                width:12%;
            }
        }
        @media  only screen and (min-width:321px) and (max-width:540px){
             input{
                width:70%;
            }
            .arrow{
                width:12%;
            }
        }
        @media  only screen and (min-width:541px) and (max-width:720px){
            input{
                width:70%;
            }
            .arrow{
                width:12%;
            }
        }
    }
</style>