<template>
    <div>
        <headers></headers>
        <img src="./timg (2).jpg">
        <p>树懒果园，泰国进口大金煌芒果</p>
        <p>5斤装 约2-4个果，大！！！甜！！！</p>
        <footers></footers>
    </div>
</template>
<script>
import headers from './headers.vue'
import footers from './footers.vue'
export default {
    components:{
        "headers":headers,
        "footers":footers
        

    },
}
</script>

<style scoped>
    img{
        width:100%;
        margin-top:7.1vh;
    }
    p{
        color:#e6ba02;
        font-size:4vh;
        text-align:center;
    }
    p+p{
        color:#333;
        font-size:2.5vh
    }

  
</style>