<template>
  <header>
    <nav class="nav">
      <ul class="nav__items">
        <li class="nav__item nav__item--active" @click="goTo('.home')">Home</li>
        <li class="nav__item" @click="goTo('.about')">About</li>
        <li class="nav__item" @click="goTo('.portfolio')">Portfolio</li>
        <li class="nav__item" @click="goTo('.contact')">Contact</li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  methods: {
    goTo(path) {
      document.querySelector(path).scrollIntoView({
        behavior: 'smooth',
        block: 'end',
      })
    },
  },
}
</script>

<style lang="scss" scoped>
.nav {
  width: 100%;
  position: fixed;
  top: 0;
  border-bottom: 3px solid #04c2c9;
  background: #1b242f;
  &__items {
    padding: 1rem;
    display: flex;
    align-items: center;
  }

  &__item {
    list-style-type: none;
    font-size: 1rem;
    text-transform: uppercase;
    color: #fff;
    cursor: pointer;
    &:hover {
      color: #e31b6d;
    }
  }

  &__item--active {
    color: #e31b6d;
  }

  &__item:not(:first-child) {
    margin-left: 5rem;
  }
}
</style>
