<template>
  <div>
    <h1>Events</h1>
    <div class="links">
      <nuxt-link v-for="post in posts"
        :to="{name: 'posts-id', params: {id: post.id}}"
        :key="post.id"
      >
        {{ post.title}}
        <br>
      </nuxt-link>
    </div>
  </div>

</template>

<script>
  export default {
      components: {

      },

      head() {
          return {
              title: 'Home Page'
          }
      },

      computed: {
          posts() {
              return this.$store.state.posts.all
          }
      }
  }
</script>


