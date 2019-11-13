<template>
    <div>
        <div id="header">
            <button>返回</button>
            <span>商品详情页</span>
        </div>

    </div>
</template>
<style scoped>

    #header{
        height:7vh;
        width:100%;
        border-bottom:1px solid #ccc; 
        text-align:center;
        position:fixed;
        top:0;
    }
    #header>button{
        position:absolute;
        left:0;
        background:0;
        color:#999;
        border:0;
        top:2vh
    }
    #header>span{
        font-size:4vh;
        line-height:7vh;
    }
</style>