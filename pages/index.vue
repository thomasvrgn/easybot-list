<template>
  <main>
    <navbar />
    <header class="bg-indigo-100 py-8 px-8 mx-auto">
      <div class="container mx-auto w-2/3">
        <h1 class="text-2xl font-semibold text-gray-700">
          Promoting your bots has never been easier
        </h1>
        <p class="text-gray-600 mt-4">
          EasyList is a site and bot allowing you to promote your bot for free in order to attract more audience and increase your influence.
        </p>
      </div>
    </header>
  </main>
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
