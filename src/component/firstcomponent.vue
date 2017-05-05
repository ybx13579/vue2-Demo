<template>
    <div id="firstcomponent">
        <div class="header">
            <div class="fl logo-outer"><img src="../img/logo1.png"></div>
            <ul class="fl nav">
                <li><a href="javascript:;">首页</a></li>
                <li><a href="javascript:;">商品页</a></li>
                <li><a href="javascript:;">详情页</a></li>
                <li><a href="javascript:;">购物车</a></li>
                <li><a href="javascript:;">首页</a></li>
            </ul>
        </div>
    </div>
</template>

<script type="text/javascript">
    export default {
        data () {
            return {
                boxmsg:'这是植物件！'
            }
        }
    }
</script>

<style>
    *{
        margin:0;
        padding:0;
    }
    body{
        font-family: '微软雅黑';
    }
    .fl{
        float: left;
    }
    .header{
        width:100%;
        height:80px;
        background: rgba(119, 81, 95, 0.43);
        margin-bottom:20px;
    }
    .logo-outer{
        margin-left: 20px;
        margin-right:100px;
    }
    .nav{
        line-height: 80px;
    }
    .nav li{
        margin-right: 20px;
    }
    .nav li a{
        color: #fff;
        font-size: 20px;
        text-decoration: none;
    }
    .nav li a:hover{
        text-decoration: underline;
    }
</style>