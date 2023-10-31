<template>
    <div class="niubi">
        <div class="ko" style="height:5px;"></div>
        <div class="mycard" v-for="item in uselist" :key="item.id">
            <div class="card">
                <div class="header">
                    <span class="left"><v-icon style="margin-bottom:2px" color="black" size="15px">mdi-account-outline</v-icon>{{item.name}}</span>
                    <span class="right"> {{item.jg}}元</span>
                </div>
                <div class="text" style="margin-top:7px"><v-icon style="margin-bottom:4px">mdi-map-marker-outline</v-icon>{{item.dot}}</div>
                <div class="text"><v-icon style="margin-bottom:4px">mdi-clock-outline</v-icon>{{item.clock}}</div>
                <div class="bttt"><v-btn  color="#FF6600" class="btt"><p class="bt">接单</p></v-btn></div>
            </div>
        </div>
</div>
</template>

<script>
export default {
data(){
    return{
        uselist: [
        { id: 1, name: '小蔡', dot:'北京大学',clock:'10.24早上8点3小时',jg:'210'},
        { id: 2, name: '龙王', dot:'幸福小区花园',clock:'11.09晚上8点6小时',jg:'380'},
        { id: 3, name: '金刚', dot:'玉龙雪山',clock:'10.10早上8点1星期',jg:'3500'},
        { id: 4, name: '小美', dot:'广东医科大学',clock:'10.04早上10点3小时',jg:'120'},

    ],
    }
}
}
</script>

<style scoped>
.bttt{
    margin-top: 10px;
    width: 100vw;
    display: flex;
    justify-content: center;
}
.btt{
    width: 90vw;
    color: #FF6600;
    z-index: 5;
}
.bt{
    font-size: 20px;
    font-weight: 600;
    color: #000;
}
.mycard{
    width: 100vw;
    height: 200px;
    margin-bottom: 10px;
    
}
.card{
    width: 100%;
    height: 100%;
    background: #fff;
    border-radius: 5px;
}
.niubi{

    width: 100vw;
    background: #dad5d5;
    height: 100vh;
}
.imgg{
    width: 50px;
    height: 50px;
    border-radius: 50%;
}
.left{
    float: left;
    margin-left:5px;
    height: 20px;
    line-height: 35px;
    color: rgb(232, 129, 12);
}
.right{
    float: right;
    margin-right:5px;
    color: red;
    font-weight: 800;
}
.header{
    width: 100%;
    height: 30px;
}
.text{
    width: 100%;
    height: 50px;
    line-height: 50px;
    font-size:20px;
    font-weight: 800;
    display: flex;
    margin-left:55px;
    align-items: center;
}
</style>