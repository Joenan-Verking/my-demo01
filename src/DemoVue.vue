<template>
  <div id="demo">
    <CardBox></CardBox>
    <a href="https://beian.miit.gov.cn/" target="_blank">粤ICP备2023012633号-1</a>
  </div>
</template>

<script>
  import CardBox from "./components/CardBox.vue";

  export default {
    name: "Demo",
    components: {
      CardBox,
    },
  };
</script>

<style>
  #demo {
    width: 100vw;
    height: 100vh;
    display: flex;
    padding: 0;
    margin: 0;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    /* background: url('./assets/background.jpg') fixed no-repeat; */
    background: linear-gradient(#ff04c44f,#ffdbc9);
    background-size: cover;
  }

  a {
    position: fixed;
    bottom: 20px;
    color: rgba(255, 255, 255, 0.856);
    text-shadow: 0 0 10px #1c1c1ce3;
    text-decoration: none;
  }
</style>