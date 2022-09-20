<template>
  <div>
    <MainSection title="Home" :loading="loading">
      This is our Homepage
    </MainSection>
  </div>
</template>

<script lang="ts" setup>
  const loading = ref( false )
</script>

<style scoped>

</style>
