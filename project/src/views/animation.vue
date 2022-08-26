<template>
  <div class="home" :style="{width:width,height:height}">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="忍者の時代はもうすぐ終わる"/> -->
    <div class="donghua1"></div>
    <div style="width:30px;height:30px;position:relative">
      <div class="iconMoveAnimation"></div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
// import mixinTest from '@/utils/mixin.js' // 局部混入

export default {
  name: 'Home',
  components: {
    // HelloWorld
  },
  // mixins: [mixinTest],
  data () {
    return {
      width: '100%',
      height: window.innerHeight + 'px'
    }
  },
  mounted () {
    window.onresize = () => { /* 实时监听浏览器窗口的变化 */
      this.height = window.innerHeight + 'px'
    }
    // console.log(this.width, this.height, '999')
  }
}
</script>
<style lang="scss" scoped>
@import "../assets/style/mixin.scss"; /* 要引入混入的东西 */
// .home{
//   @include wordcolor;  /* 使用@include来使用混入中的东西 */
//   // color:orange;
//   @include backgroundCoverStyle('../assets/homebg.jpg')
// }
// .iconMoveAnimation{
//   width:50px;
//   height:61px;
//   @include backgroundStyle('../assets/img/turnrighticon.png');
// }
</style>
