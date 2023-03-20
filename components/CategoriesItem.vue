<template>
    <button class="CategoriesItem-Button">
        {{ props.categoryTitle }}
    </button>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

interface IProps {
    categoryTitle: string
}

const props = defineProps<IProps>()
</script>

<style scoped lang="scss">
.CategoriesItem-Button {
    all: initial;
    font-size: 12px;
    background-color: #F5F5F5;
    padding: .4rem .8rem;
    cursor: pointer;
}
</style>