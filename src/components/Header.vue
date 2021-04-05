<template>
  <div>
    <header class="flex-and-space-between">
      <div class="header flex-and-center">
        <img src="https://screenshot.click/05-45-0ikmf-tru0s.png" class="header-logo">
      </div>
      <nav class="flex-and-center uppercasing navigation">
        <div class="header-nav-item pointer">Home</div>
        <div class="header-nav-item pointer">Shop</div>
        <div class="header-nav-item pointer">Reviews</div>
        <div class="header-nav-item pointer">Blog</div>
      </nav>
      <div></div>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style>
  .header {
    height: 56px;
    margin: 10px 10%;
  }

  @media (max-width: 640px) {
    .header {
      margin: 0;
    }
  }

  .header-logo {
    width: 80px;
  }

  .header-nav-item {
    margin-right: 32px;
  }

</style>
