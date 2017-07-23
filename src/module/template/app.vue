<template>
    <div class="top">
        <div class="one"><span class="arrow"></span></div>
        <div class="two"><p>123</p><span>456</span></div>
        <div class="three">
            <com-button></com-button>
            <button id="jj" @click="jqjq">jq控制台查看</button>
            <button @click="aa">axios</button>
        </div>
    </div>
</template>

<script>

import Lib from 'assets/lib.js';
//引入组件
import comButton from 'components/com_button';

export default {
    data(){
        return {

        }
    },
    components: {
        comButton
    },
    created(){

    },
    methods: {
        jqjq(){
            console.log($('#jj'));
        },
        aa(){
            axios.get('/public/sactivity/shop_list/')
            .then((res) => {
                console.log(res);
            })
            .catch((error) => {
                console.log(error);
            })
        }
    }
}
</script>

<style lang="less" scoped>
    @import '~assets/less/common.less';

    .top{
        width: 100%;
        height: 300px;
        display: flex;
        .one,
        .two,
        .three{
            flex: 1;
        }

        .one{
            background-color: pink;
            .arrow{
                .arrow(5px);
            }
        }
        .two{
            background-color: brown;
        }
        .three{
            background-color: gray;
        }

    }
</style>
