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
      </VCard>
    </div>
  </div>
</template>

<script>
useHead({
  title: "vocabulary",
});
export default {
  name: "vocabulary"
}
</script>

<style scoped>

</style>
<route lang="yaml">
meta:
layout: home
</route>