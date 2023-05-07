<script setup lang="ts">
import { toggleDark } from '~/composables'
import useEventsBus from '~/composables/core/eventBus'
import myLogo from '~/assets/img/mylogo.jpg'
const sidebarCollapsed = ref(false)
const { emit } = useEventsBus()
watch(sidebarCollapsed, (val) => {
  emit('sidebarCollapsed', val)
})

const { t } = useI18n()

</script>
<template>
  <!-- header component -->

  <header
    :class="` px-6 transition-padding duration-700 w-full  md:fixed right-0 z-20 flex flex-col items-center justify-center md:justify-between  px-4 py-2 space-y-2 shadow-md  md:py-0 md:space-y-none md:h-16 md:flex-row bg-white dark:bg-primary-900`">
    <div class="flex items-center justify-center h-16 text-5xl">
      <RouterLink to="/" class="text-primary-400" aria-label="go to home">
        <img src="/favicon.svg" width="48" alt="Home" />
      </RouterLink>
    </div>

    <div>
      <div class="relative">
        <span
          class="absolute inset-y-0 z-10 flex items-center pl-3 text-xl text-gray-500 i-carbon-search top-1/4 left-3" />
        <input type="text" placeholder="Type Something"
          class="w-full min-w-[300px] py-2 pl-10 pr-4 text-gray-700 bg-white border rounded-md dark:bg-primary-900 dark:text-gray-300 dark:border-gray-500 focus:border-blue-400 focus:ring-blue-300 focus:ring-opacity-40 dark:focus:border-blue-300 focus:outline-none focus:ring">
      </div>
    </div>

    <!--
    <div class='title'>
</div>
<div class='outerBorder'>
  <div onclick='activateToggle()' class="toggle-outer" tabindex="0" aria-role="button">
    <div id="center">
      <div class="toggle-inner">
        <div class='toggle-inner-overlay'>
          <div class="spot1"></div>
          <div class="spot2"></div>
          <div class="spot3"></div>

        </div>
      </div>
      <div class="halo1"></div>
      <div class="halo2"></div>
      <div class="halo3"></div>
    </div>

    <div class='clouds'>
      <svg xmlns="http://www.w3.org/2000/svg" version="1.2" viewBox="0 0 170 60" width="170" height="60">
        <title>New Project</title>
        <style>
          .s0 {
            fill: #e1e1e1
          }

          .s1 {
            fill: #ffffff
          }
        </style>
        <g id="Folder 1">
          <path id="Shape 2 copy" class="s0" d="m141 42.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
          <path id="Shape 3 copy 24" class="s0" d="m127 52.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
          <path id="Shape 3 copy 16" class="s0" d="m26 74.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
          <path id="Shape 3 copy 17" class="s0" d="m49 63.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
          <path id="Shape 3 copy 18" class="s0" d="m71 62.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
          <path id="Shape 3 copy 19" class="s0" d="m155 41.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
          <path id="Shape 3 copy 20" class="s0" d="m123 57.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
          <path id="Shape 3 copy 21" class="s0" d="m162 31.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
          <path id="Shape 3 copy 22" class="s0" d="m149 55.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
          <path id="Shape 3 copy 23" class="s0" d="m99 53.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        </g>
        <path id="Shape 2" class="s1" d="m153 65.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 11" class="s1" d="m143 72.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 10" class="s1" d="m159 73.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 9" class="s1" d="m141 70.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 8" class="s1" d="m30 85.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 7" class="s1" d="m55 82.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 6" class="s1" d="m78 81.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 5" class="s1" d="m163 56.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 4" class="s1" d="m119 73.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 3" class="s1" d="m166 45.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy 2" class="s1" d="m157 70.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
        <path id="Shape 3 copy" class="s1" d="m98 72.5c-9.7 0-17.5-7.8-17.5-17.5 0-9.7 7.8-17.5 17.5-17.5 9.7 0 17.5 7.8 17.5 17.5 0 9.7-7.8 17.5-17.5 17.5z" />
      </svg>
    </div>
    <div class='stars'>
      <svg xmlns="http://www.w3.org/2000/svg" version="1.2" viewBox="0 0 170 60" width="170" height="60" style="&#10;    /* background: black; */&#10;">
        <title>New Project</title>
        <style>
          .stars .s0 {
            fill: #ffffff
          }
        </style>
        <g id="Folder 1">
          <path id="Layer 2" class="s0" d="m57 20l1.4 3.6 3.6 1.4-3.6 1.4-1.4 3.6-1.4-3.6-3.6-1.4 3.6-1.4z" />
          <path id="Shape 2" class="s0" d="m65 39l1.4 3.6 3.6 1.4-3.6 1.4-1.4 3.6-1.4-3.6-3.6-1.4 3.6-1.4z" />
          <path id="Shape 3" class="s0" d="m89 11l1.4 3.6 3.6 1.4-3.6 1.4-1.4 3.6-1.4-3.6-3.6-1.4 3.6-1.4z" />
          <path id="Shape 4" class="s0" d="m90 44l0.7 4.3 4.3 0.7-4.3 0.7-0.7 4.3-0.7-4.3-4.3-0.7 4.3-0.7z" />
          <path id="Shape 5" class="s0" d="m34 30l0.7 4.3 4.3 0.7-4.3 0.7-0.7 4.3-0.7-4.3-4.3-0.7 4.3-0.7z" />
          <path id="Shape 6" class="s0" d="m61 12l0.4 2.6 2.6 0.4-2.6 0.4-0.4 2.6-0.4-2.6-2.6-0.4 2.6-0.4z" />
          <path id="Shape 7" class="s0" d="m28 36l0.4 2.6 2.6 0.4-2.6 0.4-0.4 2.6-0.4-2.6-2.6-0.4 2.6-0.4z" />
          <path id="Shape 8" class="s0" d="m46 39l0.4 2.6 2.6 0.4-2.6 0.4-0.4 2.6-0.4-2.6-2.6-0.4 2.6-0.4z" />
          <path id="Shape 9" class="s0" d="m19 54l0.4 2.6 2.6 0.4-2.6 0.4-0.4 2.6-0.4-2.6-2.6-0.4 2.6-0.4z" />
          <path id="Shape 10" class="s0" d="m16 14l0.4 2.6 2.6 0.4-2.6 0.4-0.4 2.6-0.4-2.6-2.6-0.4 2.6-0.4z" />
          <path id="Shape 11" class="s0" d="m44 15l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 12" class="s0" d="m50 56l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 13" class="s0" d="m78 25l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 14" class="s0" d="m80 50l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 15" class="s0" d="m29 62l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 16" class="s0" d="m15 47l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 17" class="s0" d="m115 51l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 18" class="s0" d="m107 59l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 19" class="s0" d="m108 8l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 20" class="s0" d="m95 32l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 21" class="s0" d="m92 38l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
          <path id="Shape 22" class="s0" d="m100 37l0.3 1.7 1.7 0.3-1.7 0.3-0.3 1.7-0.3-1.7-1.7-0.3 1.7-0.3z" />
        </g>
      </svg>
    </div>
  </div>
</div>
    -->
    <div class="flex items-center space-x-4 rtl:space-x-reverse text-slate-600 dark:text-white">
      <button class="icon-btn mx-2 !outline-none" :title="t('button.toggle_dark')" @click="toggleDark()">
        <div i="carbon-sun dark:carbon-moon" />
      </button>
      <!-- <button aria-label="notification"
        class="text-xl cursor-pointer i-carbon-notification hover:bg-slate-500 text-slate-600 dark:text-white" />
      <div class="flex items-center cursor-pointer">
        <VAvatar corner="full" :src="myLogo" alt="logo" size="xs"></VAvatar>
      </div>-->
    </div>
  </header>
</template>
<style scoped>

</style>
