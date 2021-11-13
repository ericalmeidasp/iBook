<template>
  <div class="error-page">
    <div class="container">
      <ErroLogo />
      <p>Essa página não existe</p>
      <nuxt-link to="/"> Voltar para Home</nuxt-link>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.error-page {
  display: grid;
  height: 100vh;
  justify-content: center;
  align-content: center;
  background-color: color(dark, darkest);
  
}
.container {
  display: grid;
  width: 400px;
  gap: 5rem;
  text-align: center;
  color: color(light);
  text-decoration: none;
}

</style>
