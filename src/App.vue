<template>
  <div id="app">
    <Header></Header>
    <Slider></Slider>
    <Grid-list></Grid-list>
    <FAQs></FAQs>
    <Footer></Footer>
  </div>
</template>

<script>

import Header from "./components/Header";
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
    Header
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

* {
  margin: 0%;
}

body {
  font-family: 'Roboto', sans-serif;
  font-size: 20px;
  color: #2f2f2f;
}

.flex-and-center {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
}

.flex-and-space-between {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  justify-content: space-between;
}

.pointer {
  cursor: pointer;
}

.uppercasing {
  text-transform: uppercase;
}

.wrapper {
  flex-wrap: wrap;
  align-items: center;
}

.content-margin {
  margin: 0 5%;
}

.center {
  text-align: center;
}

@media (max-width: 640px) {
  .wrapper {
    flex-direction: column;
    flex-wrap: nowrap;
  }

  .mobile-hide {
    display: none;
  }

  .mobile-display {
    display: initial;
  }
}

</style>
