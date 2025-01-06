<template>
  <div class="page-block">
    <div class="tabs">
      <div class="tab tab-active">Текущий заём</div>
      <div class="tab">Заявки</div>
      <div class="tab">Файлы</div>
      <div class="tab">Документы</div>
    </div>
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
.button {
  padding: 12px 39px;
  border-radius: 200px;
  background: rgba(240, 248, 255, 1);
  cursor: pointer;
  border: none;
  outline: none;
  user-select: none;
  font-size: 14px;
  font-weight: 600;
  line-height: 24px;
  text-align: center;
  color: var(--blue-color);
  margin-top: 24px;
  margin-bottom: 44px;

  @media (max-width: 1000px) {
    margin-top: 20px;
  }
}
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
</style>