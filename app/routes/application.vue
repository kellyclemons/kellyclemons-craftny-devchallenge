<template lang="html">
  <div class="">
    <nav class="navbar">
      <div class="navbar-left">
        <router-link :to="{ name: 'index' }">
          <img class="navbar-logo" src="https://cdn.worldvectorlogo.com/logos/reddit-2.svg" alt="">
        </router-link>
        <p class="navbar-title">graphic_design</p>
      </div>
      <div class="navbar-right">
        <router-link :to="{name: 'favorites'}" class="navbar-right-item">
          <i class="fa fa-heart-o" aria-hidden="true"></i>
          <p>Favorites</p>
        </router-link>
      </div>
    </nav>

    <router-view></router-view>

  </div>
</template>

<script>
import Index from './index.vue';
export default {

  components: {
    Index,
  },

  name: 'Application',

  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
