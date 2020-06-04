<template>
    <div class="footer">
        <p>With <i class="fas fa-heart"></i> from all of us at <span>TELLUS</span> </p>

        <i class="fab fa-twitter"></i>
        <i class="fas fa-envelope"></i>
    </div>
    
</template>

<script>
export default {
    name:"Footer"
}
</script>

<style lang="scss" scoped>
    .footer{
        width:100%;
        height:50px;
        background-color: #045B7E;
        color:#fff;
        text-align: center;
        padding: 15px;;
        span{
            font-weight: 700;
        }
        i{
            color:#DD2E44;
        }

    }
</style>