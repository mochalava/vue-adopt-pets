<template>
  <div>
    <h1>{{ animal.name }} ({{ $route.params.species }})</h1>
    <p>Age: {{ animal.age }}</p>
    <p>Breed: {{ animal.breed }}</p>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  data() {
    return {
      animal: {}
    }
  },
  computed: {
    ...mapState(['cats', 'dogs'])
  },
  mounted() {
    const species = this.$route.params.species
    const id = this.$route.params.id
    this.animal = this[species][id]
  }
}
</script>
