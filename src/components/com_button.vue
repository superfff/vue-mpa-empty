<template>
    <div>
        <button @click="aa">111</button>
    </div>
</template>

<script>

import Lib from 'assets/lib.js';

export default {
    data(){
        return {

        }
    },
    created(){

    },
    methods: {
        aa(){
            Lib.C.common_alert();
        }
    }
}
</script>

<style lang="less" scope>

</style>
