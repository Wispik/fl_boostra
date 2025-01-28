<template>
  <div class="cards-block" :class="{'bold-text': bold}">
    <div class="cards-block__text">Номер карты: 546907******4311</div>
    <div class="cards-block__text-green">
      Используется для заявки: <span>020764954</span></div>
    <div class="cards-block__text">
      Номер карты: 546907******4311
      <svg width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M7 14C3.1339 14 0 10.8661 0 7C0 3.1339 3.1339 0 7 0C10.8661 0 14 3.1339 14 7C14 10.8661 10.8661 14 7 14ZM7 12.6C8.48521 12.6 9.90959 12.01 10.9598 10.9598C12.01 9.90959 12.6 8.48521 12.6 7C12.6 5.51479 12.01 4.09041 10.9598 3.0402C9.90959 1.99 8.48521 1.4 7 1.4C5.51479 1.4 4.09041 1.99 3.0402 3.0402C1.99 4.09041 1.4 5.51479 1.4 7C1.4 8.48521 1.99 9.90959 3.0402 10.9598C4.09041 12.01 5.51479 12.6 7 12.6ZM7 6.0102L8.9796 4.0299L9.9701 5.0204L7.9898 7L9.9701 8.9796L8.9796 9.9701L7 7.9898L5.0204 9.9701L4.0299 8.9796L6.0102 7L4.0299 5.0204L5.0204 4.0299L7 6.0102Z" fill="#808993"/>
      </svg>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    bold: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style lang="scss" scoped>
.cards-block {
  display: flex;
  flex-direction: column;
  gap: 8px;

  &.bold-text {
    & .cards-block__text {
      font-weight: 700;
    }
  }
}
.cards-block__text {
  font-family: Inter;
  font-size: 16px;
  font-weight: 500;
  line-height: 24px;
  text-align: left;
  display: flex;
  align-items: center;
  gap: 12px;

  & > svg {
    cursor: pointer;
  }
}
.cards-block__text-green {
  color: var(--green-color);
  margin-bottom: 8px;

  & > span {
    font-weight: 600;
  }
}
</style>