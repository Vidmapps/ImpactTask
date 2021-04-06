<template>
  <div>
    <header class="flex-and-space-between">
      <div class="header-logo flex-and-center">
        <img src="https://screenshot.click/05-45-0ikmf-tru0s.png" class="header-logo-img">
      </div>
      <nav class="uppercasing flex-and-center navigation">
        <ul class="nav-content-mobile">
          <div @click="openNav" class="nav-burger pointer">
            <img src="https://img.icons8.com/android/24/000000/menu.png" class="nav-burger-img mobile-display"/>
          </div>
          <div class="nav-content-menu flex-and-center mobile-hide">
            <div class="header-nav-item pointer">Home</div>
            <div class="header-nav-item pointer">Shop</div>
            <div class="header-nav-item pointer">Reviews</div>
            <div class="pointer">Blog</div>
          </div>
        </ul>
      </nav>
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
    background-color: white;
    width: 100%;
  }
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

.navigation {
  margin-left: 10%;
}

@media (max-width: 640px) {
  .navigation-active {
    height: 260px;
    position: absolute;
    z-index: 1;
    width: 104%; /* TODO - check for the other solutions to fix the width */
    opacity: 1;
  }
}

.nav-content {
  padding: 20px 0;
  margin-block-start: 0;
}

@media (max-width: 640px) {
  .nav-content-mobile {
    display: flex;
    justify-content: flex-end;
  }
}

.rectangle {
  width: 20px;
  height: 3px;
  border-radius: 2px;
  margin-top: 18px;
  justify-content: center;
}

.nav-burger .line {
  width: 25px;
  height: 3px;
  background-color: #d2ebfc;
  margin: 5px;
}

.nav-content-block {
  height: 80px;
  margin-right: 30px;
  list-style: none;
}

.nav-content-block:hover .rectangle {
  background-color: #d1eafc;
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

.nav-links {
  display: flex;
  flex-direction: column;
  align-items: center;
}

@media (max-width: 640px) {
  .nav-links {
    align-items: unset;
  }
}

@media (max-width: 640px) {
  .nav-content-menu {
    padding-top: 21px;
    width: 100%;
  }
}

.fa-times {
  color: #81accd;
  font-size: 20px;
}

.nav-content-hidden-block {
  height: 42px;
}

</style>
