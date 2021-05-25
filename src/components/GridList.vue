<template>
  <div class="wrapper flex-and-space-between content-margin">
    <div class="quick-stats">
      <div class="wrapper content-margin flex-and-space-between media">
        <div class="tab">
          <img class="my-image" src="https://screenshot.click/05-31-7qqpn-e7cfa.png">
          <div class="uppercasing product-name center">Product name</div>
        </div>
        <div class="tab">
          <img class="my-image" src="https://screenshot.click/05-31-7qqpn-e7cfa.png">
          <div class="uppercasing product-name center">Product name</div>
        </div>
        <div class="tab">
          <img class="my-image" src="https://screenshot.click/05-31-7qqpn-e7cfa.png">
          <div class="uppercasing product-name center">Product name</div>
        </div>
        <div class="tab">
          <img class="my-image" src="https://screenshot.click/05-31-7qqpn-e7cfa.png">
          <div class="uppercasing product-name center">Product name</div>
        </div>
        <div class="tab mobile-hide" :style="{ display: showTab }">
          <img class="my-image" src="https://screenshot.click/05-31-7qqpn-e7cfa.png">
          <div class="uppercasing product-name center">Product name</div>
        </div>
        <div class="tab mobile-hide" :style="{ display: showTab }">
          <img class="my-image" src="https://screenshot.click/05-31-7qqpn-e7cfa.png">
          <div class="uppercasing product-name center">Product name</div>
        </div>
        <div class="tab mobile-hide" :style="{ display: showTab }">
          <img class="my-image" src="https://screenshot.click/05-31-7qqpn-e7cfa.png">
          <div class="uppercasing product-name center">Product name</div>
        </div>
        <div class="tab mobile-hide" :style="{ display: showTab }">
          <img class="my-image" src="https://screenshot.click/05-31-7qqpn-e7cfa.png">
          <div class="uppercasing product-name center">Product name</div>
        </div>
        <button v-show="!isShowMore" @click="showMore">show more...</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GridList",
  data() {
    return {
      isShowMore: false,
      showTab: ''
    }
  },
  methods: {
    showMore() {
      this.isShowMore = !this.isShowMore;
      this.showTab = 'inline';
    }
  }
}
</script>

<style scoped>

button {
  display: none;
}

@media (max-width: 640px) {
  button {
    display: inline;
    margin: 20px;
    font-size: 16px;
    opacity: 50%;
  }
}

.tab {
  width: 250px;
}

.product-name {
  font-size: 16px;
}

.my-image {
  width: 100%;
  margin: 9px 0;
}

</style>
