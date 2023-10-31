<template>
    <div class="applike">
        <div class="maycard">
            <div class="loimgcard">
                <img src="../assets/蔡男神.png" alt="">
                <p>蔡男神 ></p>
            </div>
            <v-card class="moneycard">
                
                    <div class="money" style="float:left;">
                        <div>
                            <p class="pp">预计收入（元）</p>
                            <p class="ppp">0.00</p>
                            <p class="pppp">我的账户 ></p>
                        </div>
                    </div>
                    <div class="money" style="float:right;">
                        <div>
                            <p class="pp">已完成单量</p>
                            <p class="ppp">0.00</p>
                            <p class="pppp">历史订单 ></p>
                        </div>
                    </div>
                
            </v-card>
            <div class="nullgo">
                <span class="cardbt" style="float:left;"><v-icon style="margin-bottom:3px">mdi-gavel</v-icon> 违规申诉</span>
                <span class="cardbt" style="float:right;"><v-icon style="margin-bottom:3px">mdi-star</v-icon> 我的评价</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.applike{
    width:100%;
    height:100%;
    background: #FBF6F6;
}
.maycard{
    width: 100%;
    height:200px;
    background: #fff;
}
.loimgcard{
width: 100%;
height: 50px;
line-height: 50px;
display: flex;
}
.loimgcard img{
    width: 28px;
    height: 28px;
    margin-top: 10px;
    border-radius: 50%;
    margin-left: 10px;
}
.loimgcard p{
    font-size: 16px;
    font-weight: 600;
    margin-left: 10px;
    
}
.moneycard{
    width: 95%;
    margin-left: 9px;
    height: 120px;
    background: #FF6600;
}
.money{
    width: 50%;
    height: 120px;
    display: flex;
    justify-content: center;
    align-content: center;
    text-align: center;
    line-height: 40px;
    
}
.pp{
    font-size: 13px;
    font-weight: 600;
}
.ppp{
    font-size: 30px;
    font-weight: 600;
    color: #fff;
}
.pppp{
    font-size: 12px;
    font-weight: 600;
    color: rgb(58, 55, 55);
}
.cardbt{
    width: 50%;
    height: 30px;
    background: #fff;
    margin-top: 10px;
    line-height: 30px;
    text-align: center;
    font-size: 14px;
    font-weight: 600;
    color: #FF6600;
}
</style>