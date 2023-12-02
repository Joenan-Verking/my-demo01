<template>
    <div id="buttonBox">
        <button @click="turnToCSDN">CSDN</button>
        <button @click="turnToBlog">个人博客</button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                url_toCSDN: 'https://blog.csdn.net/Ice1774',
                url_toBlog:'https://ice.tcb.xinglincloud.top'
            }
        },
        methods: {
            turnToCSDN() {
                window.open(this.url_toCSDN, '_self')
            },
            turnToBlog() {
                window.open(this.url_toBlog, '_self')
            }
        }
    }
</script>

<style>
    #buttonBox {
        margin-top: 20px;
    }

    button {
        width: 110px;
        height: 45px;
        border: none;
        border-radius: 50px;
        background-color: #0707070c;
        position: relative;
        color: white;
        font-size: medium;
        font-weight: 600;
        text-shadow: 2px 2px 10px #0000007a;
    }

    button:hover {
        cursor: pointer;
        background-color: #0000001a;
    }
</style>