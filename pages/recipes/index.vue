<template>
  <section class="recipes">
    <recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :title="recipe.title"
      :thumbnail="recipe.thumbnail"
      :previewText="recipe.previewText"
      :id="recipe.id"
    >
    </recipe>
  </section>
</template>

<script>
  import recipe from '@/components/Recipe'
  export default {
    components: {
      recipe
    },
    asyncData () {
      return new Promise((resolve,reject) => {
        setTimeout(() => {
          resolve({
            recipes: [
              {
                title: 'Title',
                thumbnail: '/img/recipe-1.jpg',
                previewText: 'Some nice text',
                id: '1'
              },
              {
                title: 'Title',
                thumbnail: '/img/recipe-2.jpg',
                previewText: 'Some nice text',
                id: '2'
              }
            ]
          })
        }, 1500)
      })
    }
  }
</script>

<style scoped>
.recipes {
  display:flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
</style>
