<template>
  <div id="app">
    <navigation></navigation>
    <slider></slider>
    <grid-list></grid-list>
    <FAQs></FAQs>
    <Footer></Footer>
  </div>
</template>

<script>

import Navigation from "./components/Navigation";
import Slider from "./components/Slider";
import GridList from "./components/GridList";
import FAQs from "./components/FAQs";
import Footer from "./components/Footer";

export default {
  components : {
    Footer,
    FAQs,
    GridList,
    Slider,
    Navigation
  }
}
</script>

<style>

</style>
