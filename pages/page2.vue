<template>
  <div class="page-block page2">
    <MainTabs />
    <div class="name">Иванов Иван Иванович</div>
    <div class="page2-text">
      Вам предварительно одобрен займ на тех же условиях
    </div>
    <div class="page2-sliders">
      <AppSlider
        title="Сумма"
        :min="1000"
        :max="30000"
        val="₽"
        :default="1000"
        :step="1000"
      />
      <AppSlider
        title="Срок"
        :min="5"
        :max="16"
        val="дней"
        :default="5"
      />
    </div>
    <div class="block-cards-radio">
      <div class="block-cards-radio__title">Получить на карту</div>
      <div class="block-cards-radio__inputs">
        <label>
          <input type="radio" name="radioCards" value="card1" v-model="selectedCard">
          <span>Номер карты: 546907******4311</span>
        </label>
        <label>
          <input type="radio" name="radioCards" value="card2" v-model="selectedCard">
          <span>Номер карты: 588775******7642</span>
        </label>
      </div>
      <div class="block-cards-radio__green-text">К возврату 3 800 рублей до 3 октября</div>
    </div>
    <div class="page3-agree">
      Я согласен со всеми условиями
      <svg width="8" height="6" viewBox="0 0 8 6" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M3.99984 3.68273L6.88734 0.795227L7.71217 1.62064L3.99984 5.33298L0.287506 1.62064L1.11234 0.795811L3.99984 3.68273Z" fill="#6F7985"/>
      </svg>
    </div>
    <button class="button-big">Получить займ</button>
    <button class="button-white">У меня есть промокод</button>
    <CardsBlock />
    <button class="button">Добавить карту</button>
    <LinksApps />
    <div class="page2-last-block">
      <div class="page2-last-block__title">Вам доступна услуга от нашего партнера</div>
      <div class="page2-last-block__content"></div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        selectedCard: 'card1'
      }
    }
  }
</script>

<style lang="scss">
.page2 {
  & .button-big {
    margin-top: 32px;
    margin-bottom: 44px;
    width: 300px;

    @media (max-width: 1000px) {
      margin-top: 24px;
    }
  }
  & .button-white {
    margin-bottom: 44px;
    display: flex;
  }
  & .button {
    margin-top: 24px;
    margin-bottom: 44px;
    display: flex;
  }
}
.page2-text {
  font-size: 16px;
  line-height: 24px;
  color: var(--text-gray-color);

  @media (max-width: 1000px) {
    font-size: 14px;

    & > span {
      display: block;
    }
  }
}
.page2-sliders {
  display: flex;
  align-items: center;
  gap: 44px;
  margin-top: 32px;
  margin-bottom: 44px;

  @media (max-width: 1000px) {
    margin-bottom: 24px;
    gap: 24px;
    flex-direction: column;
    width: 100%;
  }
}
.page3-agree {
  margin-top: 44px;
  display: flex;
  align-items: center;
  gap: 4px;
  color: var(--text-gray-color);
  font-size: 12px;
  line-height: 24px;
  text-decoration: underline;
}
.block-cards-radio {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.block-cards-radio__title {
  font-family: Inter;
  font-size: 20px;
  font-weight: 700;
  line-height: 24px;
  text-align: left;
}
.block-cards-radio__inputs {
  display: flex;
  flex-direction: column;
  gap: 16px;
  
  & label {
    cursor: pointer;
    user-select: none;
  }

  & input {
    position: absolute;
    z-index: -1;
    opacity: 0;
  }

  & span {
    display: grid;
    grid-template-columns: 16px 1fr;
    align-items: center;
    gap: 16px;
    font-size: 16px;
    line-height: 24px;

    &::before {
      content: '';
      width: 16px;
      height: 16px;
      background: var(--white-color);
      border-radius: 100%;
      border: 1px solid var(--blue-color);
    }
  }

  & input:checked+span::before {
    background: url("data:image/svg+xml;base64,PHN2ZyB3aWR0aD0nMTYnIGhlaWdodD0nMTYnIHZpZXdCb3g9JzAgMCAxNiAxNicgZmlsbD0nbm9uZScgeG1sbnM9J2h0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnJz48cmVjdCB4PScwLjUnIHk9JzAuNScgd2lkdGg9JzE1JyBoZWlnaHQ9JzE1JyByeD0nNy41JyBmaWxsPScjMDM4QUVFJy8+PHJlY3QgeD0nMC41JyB5PScwLjUnIHdpZHRoPScxNScgaGVpZ2h0PScxNScgcng9JzcuNScgc3Ryb2tlPScjMDM4QUVFJy8+PHBhdGggZD0nTTExLjc2NSA1LjIwNDc0QzEyLjA2NjEgNS40ODkxNSAxMi4wNzk3IDUuOTYzODMgMTEuNzk1MyA2LjI2NDk3TDcuNTQ1MjYgMTAuNzY1QzcuNDA2MTMgMTAuOTEyMyA3LjIxMzMyIDEwLjk5NyA3LjAxMDcxIDEwLjk5OTlDNi44MDgxIDExLjAwMjggNi42MTI5NSAxMC45MjM2IDYuNDY5NjcgMTAuNzgwM0w0LjIxOTY3IDguNTMwMzNDMy45MjY3OCA4LjIzNzQ0IDMuOTI2NzggNy43NjI1NyA0LjIxOTY3IDcuNDY5NjdDNC41MTI1NiA3LjE3Njc4IDQuOTg3NDQgNy4xNzY3OCA1LjI4MDMzIDcuNDY5NjdMNi45ODQ2MyA5LjE3Mzk3TDEwLjcwNDcgNS4yMzUwM0MxMC45ODkxIDQuOTMzOSAxMS40NjM4IDQuOTIwMzMgMTEuNzY1IDUuMjA0NzRaJyBmaWxsPSd3aGl0ZScvPjwvc3ZnPgo=") center no-repeat;
  }
}
.block-cards-radio__green-text {
  color: var(--green-color);
}
.page2-last-block {
  margin-top: 44px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.page2-last-block__title {
  font-family: Inter;
  font-size: 16px;
  font-weight: 700;
  line-height: 24px;
}
.page2-last-block__content {
  width: 578px;
  height: 250px;
  background-color: var(--background-color);
  border-radius: 32px;

  @media (max-width: 1000px) {
    width: 100%;
    height: 323px;
  }
}
</style>