<script setup lang="ts">
useHead({
  title: '워드집'
})
</script>

<template>
  <ComponentsDemo title="워드집">
      <div class="flex gap-2 gap-x-12">
        <VCard>

          <template #media>
            <img
                src="https://images.unsplash.com/photo-1577871450676-6159315fba89?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1974&q=80"
                alt="">
          </template>
          <template #header>끼끼끼 </template>
          <p class="text-sm">
            The Botanical Garden of Algiers, Algeria History of the Garden In 1831, the French colony began undertaking
            remediation work on the marshlands in order to cultivate agricultural soil. By 1832, Governor General
            Antoine Avisard signed a decree that established a test garden in a place called El Hamma, east of Algiers.

          </p>
          <template #footer>
            <div class="flex gap-2">
              <VBadge content="끼끼끼끼" variant="primary" smooth></VBadge>
              <VBadge content="끼끼끼" variant="primary" smooth></VBadge>
              <VBadge content="끼" variant="primary" smooth></VBadge>
              <VBadge content="이끼끼" variant="primary" smooth></VBadge>
            </div>
          </template>

        </VCard>

      </div>

  </ComponentsDemo>
</template>
<route lang="yaml">
meta:
layout: dashboard
</route>