<template>
    <div id="cardBox" @mouseover="cardBoxHover" @mouseleave="cardBoxLeave">
        <PicBox :isHover="isHover"></PicBox>
        <!-- 父组件向子组件传值，v-bind:isHover = value -->
        <TextBox></TextBox>
    </div>
</template>

<script>
    import PicBox from './PicBox.vue';
    import TextBox from './TextBox.vue';
    // import ButtonBox from './ButtonBox.vue';
    export default {

        name: 'cardBox',

        components: {
            PicBox,
            TextBox,
            // ButtonBox,
        },

        data() {
            return {
                isHover: false
            };
        },

        methods: {
            cardBoxHover() {
                this.isHover = true
            },
            cardBoxLeave() {
                this.isHover = false
            }
        },

        props: {
            //init:{ default: value }
        },

        computed: {

        },

        watch: {

            immediate: true
        },

        beforeCreate() {

        },  // 生命周期 - 创建之前

        created() {

        },  // 生命周期 - 创建完成（可以访问当前this实例）

        beforeMount() {

        },  // 生命周期 - 挂载之前

        mounted() {

        },  // 生命周期 - 挂载完成（可以访问DOM元素）

        beforeUpdate() {

        },  // 生命周期 - 更新之前

        updated() {

        },  // 生命周期 - 更新之后

        beforeDestroy() {

        },  // 生命周期 - 销毁之前

        destroyed() {

        },  // 生命周期 - 销毁完成

        activated() {

        },  // 如果页面有keep-alive缓存功能，这个函数会触发
    }
</script>

<style scoped>
    #cardBox {
        padding: 0;
        margin: 0;
        width: 300px;
        height: 150px;
        /* background: inherit; */
        display: flex;
        align-items: center;
        flex-direction: column;
        border-radius: 30px;
        /* box-shadow: 0px 0px 20px 15px #0a0a0a2f; */
        box-shadow: 5px 5px 6px 2px #0a0a0a4d, inset -6px -6px 5px 0px #ffffff8f, inset 4px 4px 5px 0 #0a0a0a54, -3px -3px 10px 1px #ffffff8f;
        transition: 0.4s;
        text-shadow: 2px 2px 10px #0000007a;
    }

    #cardBox:hover {
        height: 400px;
    }

    #cardBox::before {
        content: "";
        position: absolute;
        height: 150px;
        width: 300px;
        border-radius: 30px;
        background: inherit;
        filter: blur(5px);
        transition: 0.4s;
    }
    
    #cardBox:hover::before {
        filter: blur(20px);
        height: 400px;
    }
</style>