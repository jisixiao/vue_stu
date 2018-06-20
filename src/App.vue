<!-- 展示模板 -->
<template>
  <div id="app">

    <hello></hello>
    <!--<preloader></preloader>-->
    <container></container>
    <slider></slider>
    <about></about>
    <services></services>
    <protfolio></protfolio>
    <pricing></pricing>
    <team></team>
    <contact></contact>
    <footer_container></footer_container>


  </div>
</template>

<script>
// 导入组件
import Hello from './components/Hello'
import footer_container from './components/footer_container'
import contact from './components/contact'
import team from './components/team'
import pricing from './components/pricing'
import services from './components/services'
import about from './components/about'
//大图滑动显示
import slider from './components/slider'
import protfolio from './components/protfolio'
import container from './components/container'
//import preloader from './components/container'

export default {
  name: 'app',
  components: {
    Hello,
    footer_container,
    contact,
    team,
    pricing,
    services,
    about,
    slider,
    protfolio
    ,container

//    ,preloader
  }
}
</script>
<!-- 样式代码 -->
<style>

</style>
