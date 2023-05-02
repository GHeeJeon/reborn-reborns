<script setup lang="ts">
import landscape from "~/assets/img/landscape.jpg";
import CardStatsHeader from './_components/CardStatsHeader.vue';
</script>
<template>
  <div class="pt-4 px-4">
    <div class="flex gap-2 gap-x-12">
      <VCard block>
        <template #media>
          <img :src="landscape" alt="">
        </template>
        <template #header>Hills </template>
        <p class="text-sm">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. <br>
          Cupiditate aspernatur unde harum perferendis<br>
          suscipit numquam commodi aut quia consequatur, doloremque<br>
          ab beatae aliquam impedit sit quos praesentium<br>
          sequi sed fugiat.

        </p>
        <!-- <template #footer>
          <div class="flex gap-2">
            <VBadge content="Hills" variant="secondary" smooth></VBadge>
            <VBadge content="Nature" variant="secondary" smooth></VBadge>
            <VBadge content="Montains" variant="secondary" smooth></VBadge>
            <VBadge content="Trees" variant="secondary" smooth></VBadge>
          </div>
        </template>-->

      </VCard>

    </div>

  </div>
</template>
<style scoped></style>
<route lang="yaml">
meta:
  layout: dashboard
</route>
