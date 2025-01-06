<template>
  <header class="header">
    <div class="header__body">
      <img class="header__body-logo" src="~/assets/images/logo.svg">
      <div class="header__body-links only_desktop">
        <NuxtLink to="/">Партнеры</NuxtLink>
        <NuxtLink to="/">Условия</NuxtLink>
        <NuxtLink to="/">Контакты</NuxtLink>
      </div>
      <div class="header__body-info">
        <div class="header__body-info-left only_desktop">
          Задайте вопрос поддержке
          <span>Круглосуточно</span>
        </div>
        <div class="header__body-button">
          <svg width="19" height="17" viewBox="0 0 19 17" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1.22949e-06 5.49451C-0.000482012 4.77236 0.14149 4.05721 0.417787 3.39001C0.694085 2.72281 1.09928 2.11667 1.61017 1.60629C2.12106 1.09591 2.72761 0.691318 3.39509 0.415688C4.06256 0.140058 4.77786 -0.0011981 5.5 7.65439e-06H12.8333C15.8703 7.65439e-06 18.3333 2.47042 18.3333 5.49451V16.5H5.5C2.46308 16.5 1.22949e-06 14.0296 1.22949e-06 11.0055V5.49451ZM16.5 14.6667V5.49451C16.4976 4.5233 16.1103 3.59264 15.423 2.90641C14.7358 2.22017 13.8045 1.83431 12.8333 1.83334H5.5C5.01861 1.83213 4.54172 1.92597 4.09667 2.10946C3.65163 2.29296 3.24718 2.56251 2.90653 2.90265C2.56588 3.24278 2.29573 3.64683 2.11157 4.0916C1.9274 4.53637 1.83285 5.01312 1.83333 5.49451V11.0055C1.83576 11.9767 2.22302 12.9074 2.91029 13.5936C3.59755 14.2798 4.52879 14.6657 5.5 14.6667H16.5ZM11 7.33334H12.8333V9.16667H11V7.33334ZM5.5 7.33334H7.33333V9.16667H5.5V7.33334Z" fill="#1E262E"/>
          </svg>
        </div>
      </div>
      <div class="header__body-right only_desktop">
        <div class="header__body-button">
          <svg width="20" height="18" viewBox="0 0 20 18" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M9.09091 18C4.07 18 0 13.9707 0 9C0 4.0293 4.07 2.53646e-06 9.09091 2.53646e-06C10.5024 -0.00104728 11.8947 0.323798 13.1572 0.94873C14.4197 1.57366 15.5176 2.48146 16.3636 3.6H13.9C12.8502 2.68359 11.5556 2.08652 10.1716 1.88046C8.7875 1.6744 7.37279 1.86809 6.09717 2.43829C4.82155 3.0085 3.73923 3.93099 2.98006 5.09507C2.2209 6.25915 1.81715 7.61538 1.81727 9.001C1.81739 10.3866 2.22136 11.7428 2.98072 12.9067C3.74008 14.0707 4.82256 14.993 6.09827 15.563C7.37399 16.133 8.78874 16.3264 10.1728 16.1202C11.5568 15.9139 12.8513 15.3166 13.9009 14.4H16.3645C15.5184 15.5187 14.4204 16.4265 13.1577 17.0515C11.8951 17.6764 10.5026 18.0012 9.09091 18ZM15.4545 12.6V9.9H8.18182V8.1H15.4545V5.4L20 9L15.4545 12.6Z" fill="#1E262E"/>
          </svg>
        </div>
        <NuxtLink to="/">Выйти</NuxtLink>
      </div>
      <div class="header__body-burger-btn only_mobile">
        <svg width="27" height="9" viewBox="0 0 27 9" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect width="27" height="2" rx="1" fill="#1E262E"/>
          <rect y="7" width="20" height="2" rx="1" fill="#1E262E"/>
        </svg>
      </div>
    </div>
  </header>
</template>

<style lang="scss">
.header {
  width: 100%;
  max-width: 1600px;
  background-color: var(--white-color);
  box-shadow: 0px 4px 20px 0px rgba(2, 17, 59, 0.1);
  border-radius: 0 0 32px 32px;
  padding: 16px 79px;

  @media (max-width: 1000px) {
    padding: 16px 32px;
  }
}
.header__body {
  display: flex;
  align-items: center;
  gap: 64px;

  @media (max-width: 1200px) {
    gap: 30px;
  }
}
.header__body-logo {
  @media (max-width: 1000px) {
    width: 96px;
  }
}
.header__body-links {
  display: flex;
  align-items: center;
  gap: 32px;
  flex: 1;
}
.header__body-info {
  display: flex;
  align-items: center;
  gap: 16px;

  @media (max-width: 1000px) {
    margin-left: auto;
  }
}
.header__body-info-left {
  display: flex;
  flex-direction: column;
  gap: 8px;
  align-items: end;
  font-size: 10px;
  line-height: 12px;
  color: var(--text-gray-color);

  & > span {
    padding: 4px 8px;
    color: var(--text-color);
    background-color: var(--background-color);
    border-radius: 30px;
  }
}
.header__body-button {
  cursor: pointer;
  width: 48px;
  height: 48px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 100%;
  border: 2px solid var(--background-color);
}
.header__body-right {
  display: flex;
  align-items: center;
  gap: 32px;
}
</style>