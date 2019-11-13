<template>
    <div>
        <div id="footer">
            <span>1</span>
            <span>2</span>
            <span>3</span>
            <span>4</span>
        </div>
    </div>
</template>
<script>
import headers from './headers.vue'
import footers from './footers.vue'
export default {
    components:{
        "headers":headers

    },
}
</script>

<style scoped>
    #footer{
        position:fixed;
        bottom:0;
        display:flex;
        justify-content:space-around;
        width:100%;
        height:7vh;
    }
    #footer>span{
        width:25%;
        text-align:center;
        color:#e6ba02;
        font-size:4vh;
    }
</style>