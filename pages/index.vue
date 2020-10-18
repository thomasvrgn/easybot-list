<template>
  <main>
    <navbar />
    <header class="bg-gray-200 py-8 px-8 mx-auto">
      <div class="container mx-auto w-2/3 lg:w-1/4">
        <h1 class="text-2xl font-semibold text-gray-700 lg:w-3/5">
          Promoting your bots has never been easier
        </h1>
        <p class="text-gray-600 mt-4">
          EasyList is a site and bot allowing you to promote your bot for free in order to attract more audience and increase your influence.
        </p>
        <button class="bg-indigo-500 flex flex-row py-1 px-4 rounded mt-4 focus:outline-none">
          <span class="mr-2 text-white font-light">
            Start using 
          </span>
          <logo />
        </button>
      </div>
    </header>
  </main>
</template>

<script lang="ts">
import Vue from 'vue'
import navbar from '~/layouts/navbar.vue'
import logo from '~/components/logo.vue'

export default Vue.extend({
  components: {
    navbar,
    logo,
  },
})
</script>
