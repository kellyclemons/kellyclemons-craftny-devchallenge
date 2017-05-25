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

              <div v-for="post in posts" class="post-details">

              <!-- NTS: Anchor tag needs to attach to the permalink to the end of https://www.reddit.com -->
                <a :href="post.permalink" class="detail-anchor">
                  <img v-bind:src="post.thumbnail" alt="" class="post-left__img">
                </a>

                <div class="post-details__right">

                  <a :href="post.url" class="detail-anchor">
                    <p class="post-details__title">{{ post.title }}</p>
                  </a>

              <!-- NTS: Anchor tag needs to attach the author to the end of https://www.reddit.com/user/ -->
                  <a href="#" class="detail-anchor">
                    <p class="post-details__author">submitted by <span class="author-colour">{{ post.author }}</span></p>
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
      posts: [],
    };
  },

  created() {
    fetch('https://www.reddit.com/r/graphic_design/top/.json')
    .then(response => response.json())
    .then((response) => {
      this.posts = response.data.children.map(child => child.data);
    });
  },

  mounted() {

  },

  methods: {

  },

};
</script>
