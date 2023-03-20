<template>
    <div class="CategoriesSection">
        <content-wrapper>
            <div class="CategoriesSection-Categories">
                <p class="CategoriesSection-CategoriesTitle">Discover more of what matters to you</p>
                <categories-item v-for="(title, index) in categories" :key="index" :category-title="title" />
            </div>
            <div class="CategoriesSection-Border"></div>
            <div class="CategoriesSection-Links">
                <ul class="CategoriesSection-LinksList">
                    <li class="CategoriesSection-LinksListItem">
                        <NuxtLink to="/" class="CategoriesSection-LinksListItemLink">Home</NuxtLink>
                    </li>
                    <li class="CategoriesSection-LinksListItem">
                        <NuxtLink to="/" class="CategoriesSection-LinksListItemLink">Our Story</NuxtLink>
                    </li>
                    <li class="CategoriesSection-LinksListItem">
                        <NuxtLink to="/" class="CategoriesSection-LinksListItemLink">Create a Post</NuxtLink>
                    </li>
                    <li class="CategoriesSection-LinksListItem">
                        <NuxtLink to="/" class="CategoriesSection-LinksListItemLink">Register</NuxtLink>
                    </li>
                </ul>
            </div>
        </content-wrapper>
    </div>
</template>

<script setup>
import { categories } from "../data.js"
</script>

<style scoped lang="scss">
.CategoriesSection {
    position: sticky;

    &-Categories {
        display: flex;
        width: 100%;
        justify-content: flex-end;
        gap: .5rem;
        flex-wrap: wrap;
        max-width: 400px;
        padding: 2rem 0;

        &Title {
            font-size: 14px;
            margin-bottom: .5rem;
            font-weight: 600;
        }
    }

    &-Border {
        border: 1px solid #F5F5F5;
    }

    &-Links {
        padding: 2rem 0;

        &List {
            list-style-type: none;
            display: flex;
            gap: .5rem;
            justify-content: flex-end;
            max-width: 400px;
            flex-wrap: wrap;

            &ItemLink {
                all: inherit;
                font-size: 14px;
            }
        }
    }
}
</style>