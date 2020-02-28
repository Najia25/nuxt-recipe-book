<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img class="thumbnail" :src="recipe.thumbnail" :alt="recipe.title">
    </div>
    <p>{{ recipe.description}}</p>
  </section>
</template>

<script>
  export default {
    asyncData (context) {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({
            recipe: [
              {
                title: 'Title',
                thumbnail: '/img/recipe-1.jpg',
                previewText: 'Some nice text',
                id: '1',
                description: 'Awesome indeed'
              },
              {
                title: 'Title',
                thumbnail: '/img/recipe-2.jpg',
                previewText: 'Some nice text',
                id: '2',
                description: 'Awesome indeed'
              }
            ].find(el => el.id === context.params.id)
          })
        }, 1500)
      })
    }
  }
</script>

<style scoped>
.single-recipe {
  padding:30px;
  text-align: center;
}
.thumbnail {
  max-width:100%;
  height:500px;
}
</style>
