<template>
  <section class="container">
    <div>
      <app-logo/>
      <h2>home</h2>
      <p><NuxtLink :to="'/users/'">
        > users
      </NuxtLink></p>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  }
}
</script>

<style>
.container {
  text-align: center;
}
</style>
