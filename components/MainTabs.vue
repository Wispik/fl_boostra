<template>
  <div class="tabs">
    <div class="tab tab-active">Текущий заём</div>
    <div class="tab">Заявки</div>
    <div class="tab">Файлы</div>
    <div class="tab">Документы</div>
  </div>
</template>

<style lang="scss">
.tabs {
  display: flex;
  align-items: center;
  gap: 16px;

  @media (max-width: 1000px) {
    gap: 12px;
    flex-wrap: wrap;
  }
}
.tab {
  padding: 8px 24px;
  font-size: 12px;
  line-height: 24px;
  cursor: pointer;
  user-select: none;
  border: 1px solid rgba(229, 233, 237, 1);
  border-radius: 200px;
  color: var(--text-gray-color);

  &.tab-active {
    border: 2px solid var(--blue-color);
    color: var(--text-color);
  }

  @media (max-width: 1000px) {
    padding: 8px 24px;
  }
}
</style>