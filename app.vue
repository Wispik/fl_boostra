<template>
  <div class="page">
    <AppHeader />
    <div class="content">
      <NuxtPage />
    </div>
    <AppFooter />
  </div>
</template>

<style lang="scss">
.page {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  gap: 13px;
  align-items: center;
}
.content {
  width: 100%;
  flex: 1;
  display: flex;
  justify-content: center;
}
</style>
