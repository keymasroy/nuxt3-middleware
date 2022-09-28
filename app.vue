<template>
  <div>
    <NuxtLayout :name="layout">
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<script lang="ts" setup>
const layout = computed(() => {
  const metaLayout = useRoute().meta.layout;

  if (metaLayout !== null && metaLayout !== undefined) {
    return metaLayout;
  }

  return 'ustra';
});
</script>
