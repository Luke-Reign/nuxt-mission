<template>
  <div>
      <p v-if="$fetchState.pending">Fetching planets....</p>
      <!-- <pre>{{$data}}</pre> -->
      <p v-else-if="$fetchState.error">Error while fetching planets</p>
      <ul v-else>
        <li v-for="planet in planets" :key="planet.slug">
          <nuxt-link :to="planet.slug">
            {{ planet.title }}
          </nuxt-link>
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  layout: 'home',
  async fetch(){
    this.planets = await fetch('https://api.nuxtjs.dev/planets').then((res) => res.json()
    )
  },
  data(){
    return{
      planets: [],
    }
  }
}
</script>

<style>

</style>