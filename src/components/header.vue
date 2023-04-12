<template>
  <header class="header">
    <div class="header-content max-container">
      <div class="header-content__nav">
        <a href="/" class="a-logocontainer">
          <div class="logo-container">
            <img src="../assets/images/logo_white.svg" alt="Flowers" width="100%" height="auto">
          </div>
        </a>
        <menu-component/>
      </div>
    </div>
  </header>
</template>

<script>
  import MenuComponent from './menu.vue'

  export default {
    name: "HeaderComponent",
    components: {
      MenuComponent
    },
    setup() {},
  };
</script>