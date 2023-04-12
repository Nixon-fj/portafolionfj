<template>
  <div class="hamburger-menu">
    <ul class="hamburger-menu__list" :class="{ 'is-active': isActive }">
      <li class="hamburger-menu__item" @click="isActive = !isActive" v-for="(route, index) in routes" :key="index">
        <router-link :to="route.route">{{ route.name }}</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MenuComponent",
  data() {
    return {
      isActive: false,
      routes: [
        {
          route      :  '/',
          name       :  'Home'
        },
        {
          route      :  'portafolio',
          name       :  'Portafolio'
        },
      ]
    };

  },
};
</script>