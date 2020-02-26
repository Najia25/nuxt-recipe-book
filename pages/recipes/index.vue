<template>
  <section class="recipes">
    <article class="recipe">
      <div></div>
      <h1>Title</h1>
      <p>SOme nice text</p>
    </article>
    <article class="recipe">
      <div></div>
      <h1>Title</h1>
      <p>SOme nice text</p>
    </article>
  </section>
</template>

<style scoped>

.recipes{
  display:flex;
  flex-wrap: wrap;
}

.recipe {
  box-sizing:border-box;
  width:280px;
  padding:8px;
  border:1px solid #ccc;
  box-shadow: 0 2px 2px #aaa
}
</style>