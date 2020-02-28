<template>
  <nuxt-link :to="'/recipes/' + id">
    <article class="recipe">
      <div class="thumbnail" :style="{ backgroundImage: 'url(' + thumbnail + ')' }"></div>
      <h1>{{ title }}</h1>
      <p>{{ previewText }}</p>
    </article>
  </nuxt-link>
</template>

<script>
  export default {
    props: ['title','thumbnail','previewText','id']
  }
</script>

<style scoped>
  a {
    text-decoration: none;
    color: #000;
  }
  .recipe {
    box-sizing: border-box;
    width: 280px;
    padding: 8px;
    border: 1px solid #ccc;
    box-shadow: 0 2px 2px #aaa;
    margin: 10px
  }
  .thumbnail {
    height: 150px;
    width: 100%;
    background-position: center;
    background-size: cover;
  }
</style>
