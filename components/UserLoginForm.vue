<template>
    <form class="UserLoginForm" @submit.prevent="handleSubmitForm">
        <h2 v-if="isRegister" class="UserLoginForm-Title">Register</h2>
        <h2 v-if="!isRegister" class="UserLoginForm-Title">Login</h2>
        <p v-if="isRegister" class="UserLoginForm-Copy">Register for an account using your email to create posts and share
            your thoughts with
            our community.</p>
        <p v-if="!isRegister" class="UserLoginForm-Copy">Log in to your account using your email to create posts and share
            your thoughts with
            our community.</p>
        <div class="UserLoginForm-InputContainer">
            <label>E-mail</label>
            <input v-model="email" type="email" />
        </div>
        <div class="UserLoginForm-InputContainer">
            <label>Password</label>
            <input v-model="password" type="password" />
        </div>
        <div v-show="!isRegister" class="UserLoginForm-InputContainer">
            <label>Confirm Password</label>
            <input v-model="confPassword" type="password" />
        </div>
        <button class="UserLoginForm-SubmitButton" type="submit">
            Submit
        </button>
        <p class="UserLoginForm-Toggle">Already have an account? <span class="UserLoginForm-ToggleSpan"
                @click="toggleLogin">Click here</span> to login
        </p>
    </form>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const handleSubmitForm = () => {
    console.log(isRegister.value)
}

const toggleLogin = () => {
    isRegister.value = !isRegister.value
}
const isRegister = ref<boolean>(true)
const email = ref<string>('')
const password = ref<string>('')
const confPassword = ref<string>('')
</script>

<style lang="scss" scoped>
.UserLoginForm {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5rem;

    &-Title {
        text-align: center;
    }

    &-Copy {
        text-align: center;
    }

    &-InputContainer {
        display: flex;
        flex-direction: column;
        gap: .25rem;
        width: min-content;
    }

    &-SubmitButton {
        display: block;
        margin: 1rem auto;
        all: initial;
        background-color: black;
        color: white;
        padding: .5rem 1rem;
    }

    &-Toggle {
        font-size: 12px;

        &Span {
            text-decoration: underline;
            font-style: italic;
            cursor: pointer;
        }
    }
}
</style>