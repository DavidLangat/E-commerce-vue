<template>
  <div class="hero">
    <div class="hero__text">
      <router-link to="/">
        <h1>
          Hellos
        </h1>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyHero',
  props: ['merchant']
}
</script>

<style lang="scss">
.hero {
  &__text {
    @apply text-blue font-bold py-4 px-6;
  }
}
</style>
