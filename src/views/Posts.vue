<template>
  <div class="container">
    <h1>Maqolalar</h1>
    <div class="posts">
      <div v-for="post in posts" class="posts__item">
        <img :src="post.img_url" alt="" width="100" height="100%">
        <div class="posts__content">
          <router-link tag="a" :to="'/posts/' + post.id" class="posts__title">{{ post.title }}</router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import data from '../assets/data.json'
export default {
  name: 'Posts',
  data() {
    return {
      posts: data
    }
  }
}

</script>

<style scoped>
.posts {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

img {
  object-fit: cover;
  width: 100px;
  height: 100%;
  border-radius: 5px;
}

h1 {
  margin-top: 10px;
  margin-bottom: 10px;
}

.posts__item {
  display: flex;
  width: 100%;
  max-width: 270px;
  border: 1px solid gray;
  border-radius: 5px;
}

.posts__content {
  padding: 10px;
}

.posts__title {
  text-decoration: none;
  font-size: 18px;
  font-weight: bold;
  color: #000;
}

.posts__title:hover {
  color: blue;
}
</style>
