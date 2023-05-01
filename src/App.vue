<script setup lang="ts">

import { isDark } from '~/composables'

useHead({
  title: 'Reborn reborns!',
  meta: [
    { name: 'description', content: '가히리 캐릭터와 대화하기' },
    {
      name: 'theme-color',
      content: computed(() => isDark.value ? '#00aba9' : '#ffffff'),
    },
  ],
})
</script>

<template>
  <RouterView />
</template>
<style>
.primary {
  @apply bg-primary-500
}

.primary.hoverable {
  @apply hover:bg-primary-600
}

.secondary {
  @apply bg-secondary-500
}

.secondary.hoverable {
  @apply hover:bg-secondary-600
}

.info {
  @apply bg-blue-500
}

.info.hoverable {
  @apply hover:bg-blue-600
}

.warning {
  @apply bg-yellow-500
}

.warning.hoverable {
  @apply hover:bg-yellow-600
}

.error {
  @apply bg-red-500
}

.error.hoverable {
  @apply hover:bg-red-600
}
</style>
