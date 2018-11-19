<template>
  <div class="container">
    <h1>This is the contact page</h1>
    <p><nuxt-link to="/">Home page</nuxt-link></p>
    <fade-example />
  </div>
</template>

<script>
import FadeExample from "../components/FadeExample.vue";
export default {
  components: {
    FadeExample
  },
  transition: 'fadeOpacity'
}
</script>

<style>
.fadeOpacity-enter-active, .fadeOpacity-leave-active {
  transition: opacity .35s ease-out;
}

.fadeOpacity-enter, .fadeOpacity-leave-active {
  opacity: 0;
}
</style>