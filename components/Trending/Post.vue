<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <figure class="TrendingPost">
    <div class="TrendingPost-Left">
      <p class="TrendingPost-LeftNumber">0{{ props.index }}</p>
    </div>
    <div class="TrendingPost-Right">
      <p class="TrendingPost-RightAuthor">{{ props.author }}</p>
      <h4 class="TrendingPost-RighTitle">{{ props.title }}</h4>
      <p class="TrendingPost-RightFooter">
        {{ props.date }} · {{ props.timeToRead }} min read
      </p>
    </div>
  </figure>
</template>

<script setup lang="ts">
interface IArticleDetails {
  author: string
  title: string
  date: string
  timeToRead: number
  id: number
  index: number
}

const props = defineProps<IArticleDetails>()
</script>

<style lang="scss" scoped>
.TrendingPost {
  display: flex;
  gap: 1rem;

  &-Left {
    &Number {
      color: rgba(230, 230, 230, 1);
      line-height: 36px;
      font-size: 30px;
      font-weight: 500;
    }
  }

  &-Right {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;

    &Author {
        font-size: 12px;
    }

    &Footer {
        font-size: 12px;
        font-style: italic;
    }
  }
}
</style>