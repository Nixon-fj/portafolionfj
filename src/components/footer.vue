<template>
  <div class="mobile-nav-container">
        <div class="mobile-nav-container-content">
          <router-link class="mobile-nav-items" v-for="(option,index) in options" :key="index" :to="option.route">
            <div class="mobile-nav-img-container"><img :src="option.img" :alt="option.alt" width="50" height="50"></div>
            <span>{{option.name}}</span></router-link>
        </div>
    </div>
  <footer class="footer">
    <div class="footer-content">
      <ul class="footer-content__list">
        <li class="footer-content__list--item" @click="isActive = !isActive" v-for="(route, index) in routes" :key="index">
          <router-link :to="route.route">{{ route.name }}</router-link>
        </li>
      </ul>
    </div>
    </footer>
</template>

<script>
  export default {
    name: "FooterComponent",
    setup() {
      return {
        routes: [
          {
            route      :  'nixon.fernandezjimenez@gmail.com',
            name       : 'Email'
          },
          {
            route      :  'https://www.linkedin.com/in/enrique-jos%C3%A9-estrada-n%C3%BA%C3%B1ez-85610657/',
            name       : 'Linkedln'
          },
          {
            route      :  'https://github.com/Nixon-fj',
            name       : 'Github'
          },
          {
            route      :  'CodePen',
            name       : 'https://codepen.io/nixon-fj'
          }
        ],
        options:[
          {
            route 	   : '/',
            img        :  require('../assets/images/icon.svg'),
            alt        :  'home',
            name       :  'HOME'
          },
          {
            route 	   : 'portafolio',
            img        :  require('../assets/images/icon.svg'),
            alt        :  'portafolio',
            name       :  'PORTAFOLIO'
          }
        ]
      }
    },
  };
</script>