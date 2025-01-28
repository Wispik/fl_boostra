<template>
  <div class="main-text mw-200">Где безопасно скачать приложение Boostra</div>
  <div class="main-apps-links">
    <a href="" target="_blank">
      <img src="~/assets/images/rustore.svg">
      <span>RuStore</span>
    </a>
    <a href="" target="_blank">
      <img src="~/assets/images/nashstore.svg">
      <span>NashStore</span>
    </a>
    <a href="" target="_blank">
      <img src="~/assets/images/android.svg">
      <span>Android</span>
    </a>
  </div>
</template>

<style lang="scss">
.main-apps-links {
  display: flex;
  gap: 20px;
  align-items: center;
  margin-top: 16px;

  & > a {
    cursor: pointer;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    width: 82px;
    height: 82px;
    background-color: var(--text-color);
    color: var(--white-color);
    border-radius: 12px;
    font-size: 12px;
    line-height: 24px;
    user-select: none;
    padding-top: 15px;
    padding-bottom: 5px;
  }

  @media (max-width: 500px) {
    justify-content: space-between;
    gap: 10px;
  }
}
.main-text {
  font-family: Inter;
  font-size: 16px;
  font-weight: 700;
  line-height: 24px;

  @media (max-width: 1000px) {
    &.mw-200 {
      width: 200px;
    }
  }
}
</style>