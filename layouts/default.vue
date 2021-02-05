<template>
  <div>
    <nav>
      <nuxt-link to="/">Home</nuxt-link>
      <nuxt-link to="/about">About</nuxt-link>
    </nav>
    <Nuxt />
  </div>
</template>

<script>
export default {
  head: {
    title: 'Nuxt Mission',
    meta: [
      { hid: 'description', name: 'description', content: 'A mission to explore the Jamstack using Nuxt' }
    ]
  }
}
</script>
<style>

</style>
