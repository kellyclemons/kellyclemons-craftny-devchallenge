<template lang="html">
  <div class="">
    <nav class="navbar">
      <!-- NAVBAR CODE -->
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
