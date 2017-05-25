<template lang="html">
  <div class="">
    <div class="app">

      <div class="main">
        <div class="post-container">

          <div class="heading">
            <p class="heading-title">Most popular posts from the past 24 hours:</p>
          </div>

          <div class="post">
            <div class="post-right">

              <!-- Note to self: Add v-for statement later -->
              <div class="post-details">

              <!-- Note to self: Need anchor to attach permalink to https://www.reddit.com -->
              <!-- NTS: Image will need a v-bind:src once js is completed -->
                <a href="#" class="detail-anchor">
                  <img src="#" alt="" class="post-left__img">
                </a>

                <div class="post-details__right">

              <!-- NTS: Title anchor will need :href="xyz" tag -->
                  <a href="#" class="detail-anchor">
                    <p class="post-details__title">{{ title }}</p>
                  </a>

              <!-- NTS: Author anchor will need :href="xyz" tag -->
                  <a href="#" class="detail-anchor">
                    <p class="post-details__author">submitted by <span class="author-colour">{{ author }}</span></p>
                  </a>

              <!-- NTS: Add action/event for favorite button later -->
                  <div class="post-details__favorite">
                    <i class="fa fa-heart" aria-hidden="true"></i>
                  </div>

                </div>

              </div>

            </div>
          </div>

        </div>
      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: 'Index',
  data() {
    return {
      title: 'testing-title',
      author: 'testing-author',
    };
  },

  created() {

  },

  mounted() {

  },

  methods: {

  },

};
</script>
