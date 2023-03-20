<template>
  <main>
    <hero-section />
    <trending-posts />
    <content-wrapper>
      <div class="ArticleList-Wrapper">
        <article-list />
        <categories-section />
      </div>
    </content-wrapper>
  </main>
</template>

<style lang="scss" scoped>
.ArticleList-Wrapper {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 1rem;
  width: 100%;
}
</style>