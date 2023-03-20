<template>
    <div class="ArticleList">
        <ul class="AcrticleList-List">
            <article-item v-for="article in articleData" :key="article.id" v-bind="article" />
        </ul>
    </div>
</template>

<script setup lang="ts">
import { articleData } from '~/data';
</script>

<style lang="scss" scoped>
.AcrticleList {
    &-List {
        list-style-type: none;
        display: flex;
        flex-direction: column;
        gap: 2rem;
        padding: 4rem 0 0;
    }
}
</style>