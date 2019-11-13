<style scoped>
/* 搜索 */

.sou{
    display:flex;
    justify-content: space-between;
    width:90%;
    height:30px;
    padding:20px 5% 17px;
    box-shadow:0px 5px 20px #e8e8e8;
    align-items:center;
}
.jia>img,.xin>img{
    width:20px;
    margin:0 10px;
}
#search{
    width:60%;
    margin:auto;
}
#search>input{
    padding:5px 10px;
    border:1px solid #ccc;
    font-size:14px;
    display:block;
    width:100%;
    box-sizing:border-box;
}
/* 导航栏 */
.daohangall{
    display:flex;
    justify-content: space-around;
}
.mt>>>.mintui-search {
    font-size: 14px;
    color:#666
}

.daohang>>>.mint-button--default{
    background-color:#fff;
    box-shadow: 0 0 0px #fff;
}
.daohang>>>.mint-button{
    font-size:2vh;
}
.xuanzhong>>>.mint-button-text{
    font-size:3vh;
    color:#000;
    font-weight: 560;
}
.mint-button::after{
    background-color:#eee;
}
/* 导航图片 */
.zhuan{
    /* display:flex;
    justify-content:space-between; */
    font-size:0;
    width:100%;
    margin:0 auto;
    margin-top:10px;
}
.zhuang{
    margin:0 auto;
    width:100%;
    column-count: 2;  /* 设置总列数 */
    column-gap: 15px; /* 列与列之间的像素 */
    column-fill: auto; /* 按顺序对列进行填充 */
    box-sizing: border-box;
    padding:0 3.5%;
    margin-bottom:110px;

}
.img{
    display:flex;
    flex-wrap:wrap;
     align-content:space-between;
     float:left;
     margin:0 2.5%;
     width:45%;
     box-sizing:border-box;
     overflow:hidden;
     border-radius:10px 10px 0 0;
}
.daohang2 .img{
    box-shadow:5px 7px 7px #ccc;
    float:left;
    width:100%;
    break-inside: avoid;
    border-radius:10px;
    box-sizing: border-box;
   border:1px solid #ccc;
   overflow:hidden;
   margin:0;
   margin-bottom:15px;
  
}
.img>img{
    width:100%;
    margin:0 auto;
}
/* 图片 */
/* .img>img{
    width:80%;
} */
/* 图片下的文字 */
.img>p:nth-child(2),.img>div>p:nth-child(1){
    font-size:14px;
    font-weight: 1000;
    margin:5px 0 5px 0px;
    text-align: left;
    width:100%;
}
.img>span:nth-child(3),.img>div>span:nth-child(2){
    font-size:12px;
    margin-left:0px;
    text-align: left;
    background-color:pink;
}
/* 轮播图 */
.a{
    height:210px;
    width:93%;
    background-color:#fff;
    border-radius: 10px;
    overflow: hidden;
    margin:auto;
    margin-top:20px;
    padding:0 1%;
}
.a img{
    width:100%;
    height:100%;
    border-radius: 10px;
    margin:0 auto;
}
.ping{
    width:100%;
    height:20px;
    display:flex;
    justify-content: space-between;
    margin:5px 0;
    padding:0 5px 0 0;
}
.ping>div>span{
    display:inline-block;
    font-size:14px;
    margin-left:8px;
}
.daohang>>>.mint-tab-container-wrap{
    padding:0 1%;
}
.daohangall>>>.mint-button--normal{
    padding:0;
}
.daohang2{
    margin-bottom:11vh;
}
#dh2{
    margin-bottom:1.5vh;
}
#sousuo{
    width:100%;
    height:100vh;
    z-index:10;
    position:fixed;
    top:67px;
    background:#fff;
}
.re{
    width:100%;
    height:30vh;
    display:flex;
    justify-content:space-around;
    flex-wrap:wrap;
}
.re>div{
    width:30%;
    position:relative;
}
.re>div>img{
    width:100%;
    position:absolute;
    top:0;
    height:100%;
}
.re>div>p{
    color:#fff;
}
</style>




<template>
<div>
    <!-- 搜索 -->
    <div class="sou">
        <div class="jia" @click="jia"><img :src="require('../../assets/img/jia.png')" alt=""></div>
        <div id="search">
            <input type="text" class="search" placeholder="搜索" v-model.trim="title" />
        </div>
        <div class="xin" @click="xin">
            <img :src="require('../../assets/img/xin.png')" alt="">
        </div>
    </div>
    <div v-if="sousuo" id="sousuo">
        <!--美食热搜-->
        <div>
            <h3>美食热搜</h3>
            <div class="re">
                <div>
                    <img src="../../assets/img/1 (7).png">
                    <p>蛋挞</p>
                </div>
                <div>
                    <img src="../../assets/img/2 (6).png">
                    <p>手抓羊肉</p>
                </div>
                <div>
                    <img src="../../assets/img/2 (7).png">
                    <p>红烧鲤鱼</p>
                </div>
                <div>
                    <img src="../../assets/img/1 (3).png">
                    <p>草莓蛋糕</p>
                </div>
                <div>
                    <img src="../../assets/img/3 (10).png">
                    <p>螃蟹</p>
                </div>
                <div>
                    <img src="../../assets/img/1 (1).png">
                    <p>蝴蝶兰</p>
                </div>
            </div>
        </div>

    </div>
    <!-- 导航栏 -->
    <div class="daohang">
        <div class="daohangall" id="dh1" @click="long">
            <mt-button class="xuanzhong"  data-id="tab1">今日</mt-button>
            <mt-button data-id="tab2">早餐</mt-button>
            <mt-button data-id="tab3">午餐</mt-button>
            <mt-button data-id="tab4">下午茶</mt-button>
            <mt-button data-id="tab5">晚餐</mt-button>
            <mt-button data-id="tab6">夜宵</mt-button>  
        </div>
        <mt-tab-container v-model="active">
            <mt-tab-container-item id="tab1">
                <div class="zhuan">
                    <div class="img" @click="detail">
                        <img :src="require('../../assets/img/dao1.jpg')" alt="">
                        <p>蛋炒饭</p>
                        <span>惊艳味蕾，好吃到爆</span>
                    </div>
                    <div class="img">
                        <img :src="require('../../assets/img/dao2.jpg')" alt="">
                        <p>麻辣香锅</p>
                        <span>惊艳味蕾，好吃到爆</span>
                    </div>
                </div>
            </mt-tab-container-item>
            <mt-tab-container-item id="tab2">
                <div class="zhuan">
                  <div class="img">
                      <img :src="require('../../assets/img/dao2.jpg')" alt="">
                      <p>蛋炒饭</p>
                      <span>惊艳味蕾，好吃到死</span>
                  </div>
                  <div class="img">
                      <img :src="require('../../assets/img/dao1.jpg')" alt="">
                      <p>麻辣香锅</p>
                      <span>惊艳味蕾，好吃到死</span>
                      </div>  
                </div>           
            </mt-tab-container-item>            
        </mt-tab-container>      
    </div>
    <!-- 轮播图 -->
    <div class="a">
      <mt-swipe :auto="3000">
        <mt-swipe-item><img :src="require('../../assets/img/l1.jpg')" alt=""></mt-swipe-item>
         <mt-swipe-item><img :src="require('../../assets/img/l2.jpg')" alt=""></mt-swipe-item>
        <mt-swipe-item><img :src="require('../../assets/img/l3.jpg')" alt=""></mt-swipe-item>
      </mt-swipe>
    </div>
    <!--循环导航栏-->
    <div class="daohang daohang2">
        <div class="daohangall" id="dh2" @click="long2">
            <mt-button class="xuanzhong" data-id="all">推荐</mt-button>
            <mt-button data-id="1">肉食</mt-button>
            <mt-button data-id="2">素食</mt-button>
            <mt-button data-id="3">甜品</mt-button>
            <mt-button data-id="4">烘培</mt-button>  
        </div>
            <div class="zhuang">
                <div class="img"  v-for="(item,i) of list2" :key="i">
                    <img :src="`http://127.0.0.1:4000/${item.shoupic}`" alt="">
                    <div style="padding:10px;width:100%;">
                        <p>{{item.titile}}</p>
                        <span>{{item.summary}}</span>
                        <div class="ping">
                            <div style="width:100% ">
                                <span style="font-size:12px; float:lfet;margin:0;">浏览</span>
                                <span style="float:right;font-size:12px">{{item.look}}</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>   
</div>
</template>


<script>
export default {
    data(){
        return{
            active:"tab1",
            list2:[],
            sousuo:false,
            title:""
        }
    },
    created(){

        var url="z_lvtu"
        var obj={classl:"all"}
        this.axios.get(url,{params:obj})
        .then(res=>{
            this.list2=res.data.data;
        })  


    },
    methods:{
        long(e){
            if(e.target.nodeName.toLowerCase() === 'button'){
                this.active=e.target.dataset.id;
                var dh1=document.getElementById("dh1")
                var hang=dh1.querySelectorAll("button")
                for(var key of hang){
                    key.classList.remove("xuanzhong")
                }
                e.target.classList.add("xuanzhong")
            }
        },
        long2(e){
           if(e.target.nodeName.toLowerCase() === 'button'){
                this.active2=e.target.dataset.id;
                var dh1=document.getElementById("dh2")
                var hang=dh1.querySelectorAll("button")
                for(var key of hang){
                    key.classList.remove("xuanzhong")
                }
                e.target.classList.add("xuanzhong")
                // 查询旅途美食表的信息
                var url="z_lvtu"
                var cl=e.target.dataset.id;
                var obj={classl:cl}
                this.axios.get(url,{params:obj})
                .then(res=>{
                    this.list2=res.data.data;
                })    
            }
        },
        jia(){
            this.$router.push("/Weibu")
        },
        xin(){
            
        },
        detail(){
            this.$router.push("/detail")
        },
        sou(){
            this.sousuo=true;
        }
    }
}
</script>

