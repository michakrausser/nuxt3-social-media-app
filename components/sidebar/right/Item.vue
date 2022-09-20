<template>
  <div
      class="p-3 border-b hover:bg-gray-100 cursor-pointer dark:hover:bg-dim-300"
      :class="tailwindComposables"
  >
    <slot />
  </div>
</template>

<script lang="ts" setup>
  const { defaultTransition, twitterBorderColor } = useTailwindConfig()


  const tailwindComposables = computed(() =>  `${ defaultTransition } ${ twitterBorderColor }`)
</script>

<style scoped>

</style>
