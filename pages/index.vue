<template>
  <div class="page-block main-page">
    <MainTabs />
    <div class="name">Иванов Иван Иванович</div>
    <div class="card-block">
      <div class="card-block__card"></div>
      <div class="card-block__info">
        <span>Деньги у Вас через</span>
        <div class="card-block__info-timer">
          00 : 02 : 07
        </div>
      </div>
    </div>
    <div class="main-text">Номер карты: 546907******4311</div>
    <div class="main-text__green">Используется для заявки:
      <span>020764954</span>
    </div>
    <button class="button">Добавить карту</button>
    <LinksApps />
  </div>
</template>

<style lang="scss">
.name {
  font-family: Inter;
  font-size: 32px;
  font-weight: 700;
  line-height: 24px;
  margin-top: 44px;
  margin-bottom: 32px;

  @media (max-width: 1000px) {
    font-size: 24px;
    line-height: 32px;
    margin-top: 24px;
    margin-bottom: 16px;
  }
}
.card-block {
  display: grid;
  grid-template-columns: 500px auto;
  gap: 64px;
  align-items: center;
  margin-bottom: 32px;

  @media (max-width: 1000px) {
    display: flex;
    flex-direction: column;
    gap: 15px;
  }
}
.card-block__card {
  width: 100%;
  height: 174px;
  border-radius: 32px;
  background-color: rgba(243, 245, 248, 1);

  @media (max-width: 1000px) {
    height: 220px;
  }
}
.card-block__info {
  display: flex;
  flex-direction: column;
  gap: 16px;

  & > span {
    color: var(--text-gray-color);
  }

  @media (max-width: 1000px) {
    width: 100%;
    gap: 12px;

    & > span {
      font-size: 14px;
      line-height: 24px;
    }
  }
}
.card-block__info-timer {
  font-family: Inter;
  font-size: 46px;
  font-weight: 600;
  line-height: 24px;

  @media (max-width: 1000px) {
    font-size: 34px;
  }
}
.main-text__green {
  font-family: Inter;
  font-size: 14px;
  font-weight: 500;
  line-height: 24px;
  text-align: left;
  color: var(--green-color);
  margin-top: 8px;

  & > span {
    font-weight: 700;
  }
}
.main-page {
  & .button {
    margin-top: 24px;
    margin-bottom: 44px;

    @media (max-width: 1000px) {
      margin-top: 20px;
    }
  }
}
</style>