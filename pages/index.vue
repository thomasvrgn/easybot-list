<template>
  <navbar />
</template>

<script lang="ts">
import Vue from 'vue'
import navbar from '~/layouts/navbar.vue'

export default Vue.extend({
  components: {
    navbar,
  },
})
</script>
