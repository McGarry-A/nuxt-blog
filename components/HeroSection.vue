<template>
  <div class="HeroSection-Wrapper">
    <content-wrapper>
      <div class="HeroSection">
        <h1 class="HeroSection-Title">Stay Curious</h1>
        <p class="HeroSection-Subtitle">
          Discover stories, thinking and expertise from writers on any topic
        </p>
        <div class="HeroSection-ButtonContainer">
          <NuxtLink to="/publish" class="HeroSection-ButtonContainerButton"
            >Create a Post</NuxtLink
          >
          <NuxtLink
            to="/register"
            class="HeroSection-ButtonContainerButton HeroSection-ButtonContainerButton_Secondary"
            >Register</NuxtLink
          >
        </div>
      </div>
    </content-wrapper>
  </div>
</template>

<style lang="scss" scoped>
.HeroSection {
  padding: 6rem 0;
  display: flex;
  flex-direction: column;
  gap: 1rem;

  &-Wrapper {
  }

  &-Title {
    font-size: 62px;
  }

  &-Subtitle {
    font-size: 22px;
    font-weight: 300;
    color: rgb(67, 66, 66);
    max-width: 500px;
    line-height: 20px;
  }

  &-ButtonContainer {
    display: flex;
    gap: 0.5rem;

    &Button {
      all: initial;
      background: rgb(58, 58, 58);
      padding: 0.75rem 1.2rem;
      border-radius: 20px;
      color: white;
      cursor: pointer;

      &_Secondary {
        background: white;
        color: black;
        border: 1px solid black;
      }
    }
  }
}
</style>