<template>
  <div class="container">
    <div>
      <img :src="post.img_url" width="400" alt="">
      <h3 style="text-align: center">{{ post.title }}</h3>
      <p>{{ post.description }}</p>
    </div>
  </div>
</template>

<script>
import data from '@/assets/data.json'

export default {
  name: 'Post',
  computed: {
    postId() {
      return parseInt(this.$route.params.id)
    },
    post() {
      return data.find(post => post.id === this.postId)
    }
  }
}
</script>