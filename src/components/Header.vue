<template>
    
    <div class="header">
        <h2 class="logo">tellus</h2>
        <button>ADD YOUR STORY</button>
    </div>

</template>

<script>

export default {
    name: "Header"
}
</script>

<style lang="scss" scoped>
$primary-color: #045B7E;

.header{
    width:100%;
    height:70px;
    padding:20px 100px;
    //border:1px solid red;
    h2{
        color:$primary-color;
        float:left;
    }
    button{
        float:right;
        color:#fff;
        background-color: $primary-color;
        height:35px;
        font-family: 'Poppins', sans-serif;
        border:none;
        margin-top:5px ;
        transition:0.2s ease-in-out;
        cursor:pointer;
        border-radius:5px;
        padding: 0 10px;
        font-size:11px;
        font-weight: 500;
    }
    button:hover{
        background-color:transparent;
        border:1px solid $primary-color;
        color:$primary-color;
    }
    @media  only screen and (max-width:320px){
        padding: 20px;
    }
    @media  only screen and (min-width:321px) and (max-width:540px){
        padding: 20px 30px;
    }
     @media  only screen and (min-width:541px) and (max-width:720px){
         padding: 20px 50px;
    }

}

</style>