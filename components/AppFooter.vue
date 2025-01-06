<template>
  <footer class="footer">
    <div class="footer__body">
      <div class="footer__links">
        <NuxtLink to="/">Информация</NuxtLink>
        <NuxtLink to="/">Документы</NuxtLink>
        <NuxtLink to="/">COVID-19 поддержка клиентов</NuxtLink>
        <NuxtLink to="/">Контакты</NuxtLink>
        <NuxtLink to="/">Сотрудничество</NuxtLink>
      </div>
      <div class="footer__info">
        <p>ООО “ФИНТЕХ-МАРКЕТ” осуществляет деятельность в сфере ИТ: сервис предоставляет онлайн-услуги по подбору</p>
        <p>финансовых продуктов, а также распространению рекламы организаций-партнеров в сети интернет</p>
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
.footer {
  max-width: 1506px;
  width: 100%;
  padding: 12px 32px 21px 32px;

  @media (max-width: 1000px) {
    padding: 32px;
  }
}
.footer__body {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
  color: var(--text-gray-footer-color);
  font-size: 9px;
  line-height: 11px;

  @media (max-width: 1000px) {
    flex-direction: column;
    align-items: start;
  }
}
.footer__links {
  display: flex;
  align-items: center;
  gap: 32px;

  & > a {
    white-space: nowrap;
  }

  @media (max-width: 1000px) {
    gap: 28px;
    flex-wrap: wrap;

    & > a {
      min-width: 58px;
    }
  }
}
.footer__info {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  text-align: end;

  @media (max-width: 1000px) {
    font-size: 10px;
    line-height: 20px;
    text-align: left;
  }
}
</style>