<template>
  <div class="TrendingPosts">
    <content-wrapper>
      <div>
        <p class="TrendingPosts-Title">Trending Posts</p>
        <div>
          <ul class="TrendingPosts-List">
            <li
              v-for="(item, index) in data"
              :key="item.id"
              class="TrendingPosts-ListItem"
            >
              <trending-post v-bind="item" :index="(index += 1)" />
            </li>
          </ul>
        </div>
      </div>
    </content-wrapper>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const data = ref([
  {
    author: 'Ahmed McGarry',
    title: 'Learn Nuxt creating a blog',
    date: new Date().toDateString(),
    timeToRead: 3,
    id: 1,
  },
  {
    author: 'Ahmed McGarry',
    title: 'Learn Nuxt creating a blog',
    date: new Date().toDateString(),
    timeToRead: 3,
    id: 1,
  },
  {
    author: 'Ahmed McGarry',
    title: 'Learn Nuxt creating a blog',
    date: new Date().toDateString(),
    timeToRead: 3,
    id: 1,
  },
  {
    author: 'Ahmed McGarry',
    title: 'Learn Nuxt creating a blog',
    date: new Date().toDateString(),
    timeToRead: 3,
    id: 1,
  },
  {
    author: 'Ahmed McGarry',
    title: 'Learn Nuxt creating a blog',
    date: new Date().toDateString(),
    timeToRead: 3,
    id: 1,
  },
  {
    author: 'Ahmed McGarry',
    title: 'Learn Nuxt creating a blog',
    date: new Date().toDateString(),
    timeToRead: 3,
    id: 1,
  },
])
</script>

<style scoped lang="scss">
.TrendingPosts {
  &-Title {
    margin: 0 0 3rem;
  }
  &-List {
    list-style-type: none;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 2rem;
  }
}
</style>