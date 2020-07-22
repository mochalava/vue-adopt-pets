<template>
  <div>
    <PetTable species="dogs" :pets="dogs"></PetTable>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  data() {
    return {}
  },
  computed: {
    ...mapState(['dogs'])
  }
}
</script>
