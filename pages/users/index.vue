<template>
  <section class="container">
    <div>
      <app-logo/>
      <h2>users page</h2>
      <p>count: {{count}}</p>
      <button @click="addCount">カウントアップ</button>
      <p><NuxtLink :to="'/'">
        > home
      </NuxtLink></p>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  },
  computed: {
    count () {
      return this.$store.state.counter.count
    }
  },
  methods: {
    addCount (e) {
      this.$store.commit('counter/add')
    }
  }
}
</script>

<style>
.container {
  text-align: center;
}
</style>
