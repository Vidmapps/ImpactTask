<template>
  <div>
    <header v-show="!isOpenNav">
      <div class="header-top flex-and-space-between">
        <div class="header-logo flex-and-center">
          <img src="https://screenshot.click/05-45-0ikmf-tru0s.png" class="header-logo-img">
        </div>
        <nav class="uppercasing flex-and-center navigation">
          <ul class="nav-content-mobile">
            <div @click="openNav" class="nav-burger pointer">
              <img v-show="!isOpenNav" src="../assets/menu_black_24dp.svg" class="nav-burger-img mobile-display"/>
              <img v-show="isOpenNav" src="../assets/close_black_24dp.svg" class="nav-burger-img mobile-display"/>
            </div>
            <div class="nav-content-menu flex-and-center mobile-hide">
              <div class="header-nav-item pointer">Home</div>
              <div class="header-nav-item pointer">Shop</div>
              <div class="header-nav-item pointer">Reviews</div>
              <div class="header-nav-item pointer">Blog</div>
            </div>
          </ul>
        </nav>
      </div>
      <div v-show="isOpenNav" class="nav-content-dropdown">
        <div v-show="isOpenNav" class="nav-content-menu center uppercasing">
          <div class="header-nav-item pointer">Home</div>
          <div class="header-nav-item pointer">Shop</div>
          <div class="header-nav-item pointer">Reviews</div>
          <div class="header-nav-item pointer">Blog</div>
        </div>
      </div>
    </header>
    <header v-show="isOpenNav">
      <div class="header-top flex-and-space-between">
        <div class="header-logo flex-and-center">
          <img src="https://screenshot.click/05-45-0ikmf-tru0s.png" class="header-logo-img">
        </div>
        <nav class="uppercasing flex-and-center navigation">
          <ul class="nav-content-mobile">
            <div @click="openNav" class="nav-burger pointer">
              <img v-show="!isOpenNav" src="../assets/menu_black_24dp.svg" class="nav-burger-img mobile-display"/>
              <img v-show="isOpenNav" src="../assets/close_black_24dp.svg" class="nav-burger-img mobile-display"/>
            </div>
            <div class="nav-content-menu flex-and-center mobile-hide">
              <div class="header-nav-item pointer">Home</div>
              <div class="header-nav-item pointer">Shop</div>
              <div class="header-nav-item pointer">Reviews</div>
              <div class="header-nav-item pointer">Blog</div>
            </div>
          </ul>
        </nav>
      </div>
      <div v-show="isOpenNav" class="nav-content-dropdown">
        <div v-show="isOpenNav" class="nav-content-menu center uppercasing">
          <div class="header-nav-item pointer">Home</div>
          <div class="header-nav-item pointer">Shop</div>
          <div class="header-nav-item pointer">Reviews</div>
          <div class="header-nav-item pointer">Blog</div>
        </div>
      </div>
    </header>
    <div class="nav-content-block"></div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isOpenNav: false
    }
  },
  methods: {
    openNav() {
      console.log(this.isOpenNav)
      return this.isOpenNav = !this.isOpenNav;
    }
  }
}
</script>

<style>
header {
  -webkit-box-shadow: 0 1px 8px -4px rgba(0, 0, 0, 1);
  box-shadow: 0 1px 8px -4px rgba(0, 0, 0, 1);
  position: sticky;
}

@media (max-width: 640px) {
  header {
    position: fixed;
    background-color: rgba(255,255,255,0.8);
    width: 100%;
  }
}

.header-top {
  background-color: white;
}

.header-logo {
  height: 40px;
  margin: 10px 10%;
}

@media (max-width: 640px) {
  .header-logo {
    margin: 24px 10px 16px;
  }
}

.header-logo-img {
  width: 80px;
}

.header-nav-item {
  margin-right: 32px;
}

@media (max-width: 640px) {
  .header-nav-item {
    margin: 10px;
    font-size: xx-large;
  }
}

.navigation {
  margin: 10px 10%;
}

.nav-content-dropdown {
  height: 240px;
}

@media (max-width: 640px) {
  .navigation {
    margin: 0;
  }
}

@media (max-width: 640px) {
  .nav-content-mobile {
    display: flex;
    justify-content: flex-end;
  }
}

.nav-content-block {
  display: none;
}

@media (max-width: 640px) {
  .nav-content-block {
    height: 80px;
    margin-right: 30px;
    list-style: none;
    display: block;
  }
}

.nav-burger {
  display: none;
}

@media (max-width: 640px) {
  .nav-burger {
    display: unset;
    margin-right: 18px;
    margin-top: 10px;
    order: 2;
  }
}

@media (max-width: 640px) {
  .nav-content-menu {
    padding-top: 21px;
    width: 100%;
  }
}

</style>
