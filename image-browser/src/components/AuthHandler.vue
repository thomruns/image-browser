<template>
  <div>
    Please wait...
  </div>
</template>

<script>
import { mapActions } from 'vuex'

export default {
  name: 'AuthHandler',
  methods: mapActions(['finalizeLogin']),
  created() { 
    // Vue lifecycle method
    this.finalizeLogin(window.location.hash) // pass everything to the right of #
  }
}
</script>
