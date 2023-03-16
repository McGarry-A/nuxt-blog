<template>
  <nav class="Navbar">
    <content-wrapper>
      <ul class="Navbar-List">
        <li class="Navbar-ListItem">
          <NuxtLink class="Navbar-ListItemLink" to="/">Home</NuxtLink>
        </li>
        <li class="Navbar-ListItem">
          <NuxtLink class="Navbar-ListItemLink" to="/about">Our Story</NuxtLink>
        </li>
        <li class="Navbar-ListItem">
          <NuxtLink class="Navbar-ListItemLink" to="/create-a-post"
            >Create a Post</NuxtLink
          >
        </li>
        <li class="Navbar-ListItem">
          <NuxtLink
            class="Navbar-ListItemLink Navbar-ListItemLinkButton"
            to="/register"
            >Sign In</NuxtLink
          >
        </li>
      </ul>
    </content-wrapper>
  </nav>
</template>

<style lang="scss" scoped>
.Navbar {
  padding: 1.4rem 0;
  &-List {
    display: flex;
    list-style-type: none;
    gap: 2rem;
    justify-content: flex-end;
    align-items: center;
    &Item {
      &Link {
        all: initial;
        cursor: pointer;
        font-size: 14px;

        &Button {
          background: rgb(20, 20, 20);
          padding: 0.45rem 1.2rem;
          border-radius: 20px;
          color: white;
        }
      }
    }
  }
}
</style>