<template>
  <header class="site-header">
    <div class="container site-header__container">
      <router-link tag="a" class="site-header__link" to="/">Bosh sahifa</router-link>
      <router-link tag="a" class="site-header__link" to="/posts">Maqolalar</router-link>
    </div>
  </header>
</template>

<style>
.site-header {
  background-color: blue;
  color: #fff;
}

.site-header__container {
  padding-top: 20px;
  padding-bottom: 20px;
}

.site-header__link {
  color: #fff;
  padding: 10px;
  font-weight: 600;
  display: inline-block;
  text-decoration: none;
  border-radius: 5px;
}

.router-link-exact-active {
  background-color: #fff;
  color: #000 !important;
}
</style>