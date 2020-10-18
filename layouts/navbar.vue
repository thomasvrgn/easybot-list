<template>
  <nav class="bg-gray-800 flex flex-col py-4 lg:py-2 px-4 lg:flex-row">
    <div class="flex flex-auto justify-center lg:flex-initial lg:w-1/5">
      <span class="flex flex-auto w-1/3 lg:hidden">
        <span class="flex items-center text-gray-400 cursor-pointer" @click=openMenu>
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M2 6C2 5.44772 2.44772 5 3 5H21C21.5523 5 22 5.44772 22 6C22 6.55228 21.5523 7 21 7H3C2.44772 7 2 6.55228 2 6Z" fill="currentColor" /><path d="M2 12.0322C2 11.4799 2.44772 11.0322 3 11.0322H21C21.5523 11.0322 22 11.4799 22 12.0322C22 12.5845 21.5523 13.0322 21 13.0322H3C2.44772 13.0322 2 12.5845 2 12.0322Z" fill="currentColor" /><path d="M3 17.0645C2.44772 17.0645 2 17.5122 2 18.0645C2 18.6167 2.44772 19.0645 3 19.0645H21C21.5523 19.0645 22 18.6167 22 18.0645C22 17.5122 21.5523 17.0645 21 17.0645H3Z" fill="currentColor" /></svg>
        </span>
      </span>
      <span class="text-white flex items-center text-2xl uppercase tracking-widest flex-auto w-1/3 justify-center">
        <span class="font-semibold">
          Easy
        </span>
        <span class="font-thin text-gray-300">
          List
        </span>
      </span>
      <span class="flex flex-auto w-1/3 lg:hidden">
        <span></span>
      </span>
    </div>
    <div class="flex flex-auto py-4 px-2 lg:w-2/5 lg:flex-initial" :class="{'hidden': !opened}">
      <ul class="space-y-3 flex-col lg:flex-row flex lg:space-y-0 lg:space-x-5 lg:items-center">
        <li class="text-gray-400 font-light hover:text-gray-400 cursor-pointer">
          Home
        </li>
        <li class="text-gray-500 font-light hover:text-gray-400 cursor-pointer">
          Ranking
        </li>
        <li class="text-gray-500 font-light hover:text-gray-400 cursor-pointer">
          Latest bots
        </li>
        <li class="text-gray-500 font-light hover:text-gray-400 cursor-pointer">
          Support
        </li>
      </ul>
    </div>
    <div class="flex flex-auto py-4 flex-col lg:flex-row lg:w-2/5 lg:flex-initial" :class="{'hidden': !opened}">
      <div class="container flex flex-row lg:flex-initial">
        <span class="bg-gray-900 items-center flex text-gray-800 px-2 rounded-l-full pt-1 cursor-pointer">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" clip-rule="evenodd" d="M18.319 14.4326C20.7628 11.2941 20.542 6.75347 17.6569 3.86829C14.5327 0.744098 9.46734 0.744098 6.34315 3.86829C3.21895 6.99249 3.21895 12.0578 6.34315 15.182C9.22833 18.0672 13.769 18.2879 16.9075 15.8442C16.921 15.8595 16.9351 15.8745 16.9497 15.8891L21.1924 20.1317C21.5829 20.5223 22.2161 20.5223 22.6066 20.1317C22.9971 19.7412 22.9971 19.1081 22.6066 18.7175L18.364 14.4749C18.3493 14.4603 18.3343 14.4462 18.319 14.4326ZM16.2426 5.28251C18.5858 7.62565 18.5858 11.4246 16.2426 13.7678C13.8995 16.1109 10.1005 16.1109 7.75736 13.7678C5.41421 11.4246 5.41421 7.62565 7.75736 5.28251C10.1005 2.93936 13.8995 2.93936 16.2426 5.28251Z" fill="currentColor" /></svg>
        </span>
        <input type="text" class="bg-gray-900 w-full py-2 rounded-r-full focus:outline-none placeholder-gray-600 text-gray-500" placeholder="Look for bots...">
      </div>
      <div class="container flex flex-row pt-8 lg:pt-0 px-2 items-center lg:flex-initial lg:justify-center">
        <div class="flex flex-row items-center lg:flex-initial">
          <img src="~/assets/user.png" class="w-12 rounded-full shadow-xl border border-gray-700" alt="">
          <span class="h-3 flex flex-row">
            <span class="items-center text-xl flex ml-4 font-semibold text-gray-400">
              Thomas.
            </span>
            <span class="text-xs flex font-light text-gray-500">
              #5520
            </span>
          </span>
        </div>
        <div class="flex flex-row flex-auto justify-end lg:hidden">
          <ul class="space-x-4 text-sm font-light">
            <a href="" class="text-gray-400 hover:text-gray-300">
              Profile
            </a>
            <a href="" class="py-1 px-4 text-sm font-light text-white rounded bg-red-600 hover:bg-red-700">
              Logout
            </a>
          </ul>
        </div>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data: () => ({
    opened: false,
  }),
  methods: {
    openMenu: function(): void {
      this.opened = !this.opened;
    }
  },
})
</script>