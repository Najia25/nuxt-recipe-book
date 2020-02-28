<template>
  <header>
    <nav>
      <ul>
        <li><nuxt-link to="/about">About</nuxt-link></li>
        <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
        <li><nuxt-link to="/">Home</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
nav{
  margin-bottom:20px;
}
ul{
  list-style: none;
  display: flex;
  justify-content: center;
  background: rgb(255, 212, 20);
  padding:10px;
}
a{
  text-decoration: none;
  color:#fff;
  font-size:18px;
}
li{
  margin-right:10px;
}
</style>