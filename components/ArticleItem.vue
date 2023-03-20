<template>
    <li class="ArticleItem">
        <div class="ArticleItem-Left">
            <p class="ArticleItem-LeftAuthor">{{ props.author }}</p>
            <h3 class="ArticleItem-LeftTitle">{{ props.title }}</h3>
            <p class="ArticleItem-LeftDescription">{{ props.description }}</p>
            <div class="ArticleItem-LeftFooter">
                <p class="ArticleItem-LeftFooterCopy">{{ props.date }} · {{ props.minutesToRead }} min read</p>
                <p class="ArticleItem-LeftFooterIcon">Bookmark</p>
            </div>
        </div>
    </li>
</template>

<script setup lang="ts">
interface IArticle {
    author: string
    description: string
    title: string
    date: string
    minutesToRead: number
    id: number
    image: string
    categories: string[]
}

const props = defineProps<IArticle>()
</script>

<style scoped lang="scss">
.ArticleItem {
    &-Left {
        display: flex;
        flex-direction: column;
        gap: .2rem;

        &Author {
            font-size: 14px;
            font-weight: 500;
        }

        &Title {
            margin-bottom: 5px;
        }

        &Description {
            font-size: 14px;
            color: rgb(119, 118, 118);
            line-height: 16px;
            margin-bottom: 5px;
        }

        &Footer {
            font-size: 12px;
            display: flex;
            justify-content: space-between;
            align-items: baseline;
        }
    }
}
</style>