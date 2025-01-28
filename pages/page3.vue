<template>
  <div class="page-block page3">
    <MainTabs />
    <div class="name">Иванов Иван Иванович</div>
    <div class="page3-text">
      Поздравляем! По вашей заявке <span>одобрено 1 000 руб.</span>
      <p>Вы можете принять решение до 24.09.2024.</p>
    </div>
    <button class="button-big">Получить займ</button>
    <CardsBlock bold/>
    <button class="button">Добавить карту</button>
    <LinksApps />
  </div>
</template>

<style lang="scss">
.page3 {
  & .button-big {
    margin-top: 32px;
    margin-bottom: 44px;

    @media (max-width: 1000px) {
      margin-top: 24px;
    }
  }
  & .button {
    margin-top: 24px;
    margin-bottom: 44px;
    display: flex;
  }
}
.page3-text {
  font-size: 16px;
  line-height: 24px;

  @media (max-width: 1000px) {
    font-size: 14px;

    & > span {
      display: block;
    }
  }
}
</style>