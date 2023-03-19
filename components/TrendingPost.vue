<template>
  <figure class="TrendingPost">
    <div class="TrendingPost-Left">
      <p class="TrendingPost-LeftNumber">{{ props.index }}</p>
    </div>
    <div class="TrendingPost-Right">
      <h4 class="TrendingPost-RighTitle">{{ props.title }}</h4>
      <p class="TrendingPost-RightAuthor">{{ props.author }}</p>
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
</style>