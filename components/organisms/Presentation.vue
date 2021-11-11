<template>
  <div class="presentation">
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nam architecto,
      laboriosam, ducimus impedit dignissimos earum maxime nesciunt perspiciatis
      eaque ratione nostrum debitis dolores id odio illo autem dolore iste
      soluta! Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis
      rerum aut doloremque eius maiores corporis eaque corrupti deserunt dolorem
      fugit, beatae ut voluptate amet excepturi totam voluptatum natus, magnam
      accusamus?
    </p>
    <img src="@/assets/img/presentation.svg" alt="Apresentação" />
  </div>
</template>

<style lang="scss" scoped>
.presentation {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 2rem;
  align-items: center;
  @include screen('small', 'medium') {
    grid-template-columns: 1fr;
  }
  p {
    line-height: 26px;
  }
  img {
    max-width: 100%;
  }
}
</style>
