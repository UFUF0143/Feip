<template>
  <footer>
    <div class="footer-container">
      <!-- Логотип -->
      <div class="logo-icon-footer" grid-area="logo">
        <LogoFooter />
      </div>

      <!-- Ссылки -->
      <nav class="footer-links" grid-area="links">
        <a class="mobile-link" href="#">Реализованные проекты</a>
        <a class="mobile-link" href="#">Новости</a>
        <a class="mobile-link" href="#">Контакты</a>
      </nav>

      <!-- Контактная информация -->
      <div class="footer-info" grid-area="info">
        <div class="telephone-group">
          <img class="telephone-footer" src="/image/telephone.png" alt="telephone">
          <span class="number-phone-footer">+7 (900) 900-90-90</span>
        </div>
        <div class="telephone-group">
          <img class="email" src="/image/email.png" alt="email">
          <span class="email-info">info@gmail.com</span>
        </div>
        <div class="telephone-group">
          <img class="adress" src="/image/adress.png" alt="adress">
          <span class="adress-info">г. Владивосток<br>ул. Выселковая 49, стр. 3</span>
        </div>
      </div>

      <!-- Кнопка "Оставить заявку" -->
      <div class="footer-but" grid-area="button">
        <Button>Оставить заявку</Button>
      </div>

      <!-- Нижняя строка с правами и ссылками -->
      <div class="button-group" grid-area="bottom">
        <p class="footer-link">© Загдом, 2021</p>
        <a class="footer-politic" href="#">Политика конфиденциальности</a>
        <a class="agree" href="#">Пользовательское соглашение</a>
      </div>
    </div>
  </footer>
</template>
<style>
footer {
  background-color: rgba(37, 71, 65, 1);
  padding: 20px 0;
}

.footer-container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: auto auto;
  gap: 20px;
  padding-inline: 88px;
  grid-template-areas:
    "logo links info button"
    "bottom bottom bottom bottom";
  max-width: 1440px;
  margin: 0 auto;
}

/* Определение областей */
.logo-icon-footer {
  grid-area: logo;
}
.footer-links {
  grid-area: links;
}
.footer-info {
  grid-area: info;
}
.footer-but {
  grid-area: button;
}
.button-group {
  grid-area: bottom;
}

/* Стили для логотипа */
.logo-icon-footer {
  margin-top: 37px;
  display: flex;
  align-items: flex-start;
}

/* Стили для ссылок */
.footer-links {
  display: flex;
  flex-direction: column;
  gap: 24px;
  font-family: Open Sans, sans-serif;
  color: white;
  font-size: 16px;
  margin-top: 49px;
}

.footer-links a {
  color: white;
  text-decoration: none;
  transition: opacity 0.3s;
}

.footer-links a:hover {
  opacity: 0.8;
}

/* Стили для контактной информации */
.footer-info {
  display: flex;
  flex-direction: column;
  gap: 24px;
  color: white;
  font-family: Monserrat, sans-serif;
  font-size: 14px;
  margin-top: 48px;
}

.telephone-group {
  display: flex;
  align-items: flex-start;
}

.telephone-group img {
  width: 16px;
  height: 16px;
  margin-top: 2px;
}

.number-phone-footer,
.email-info,
.adress-info {
  margin-left: 8px;
  line-height: 1.4;
}

/* Стили для кнопки */
.footer-but {
  display: flex;
  justify-content: flex-end;
  margin-top: 32px;
}

/* Стили для нижней строки */
.button-group {
  width: 70%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  opacity: 0.6;
  font-family: Open Sans, sans-serif;
  color: white;
  font-size: 14px;
  padding: 20px 0 0;
  margin-top: 20px;
}

.footer-link,
.footer-politic,
.agree {
  text-decoration: none;
  color: white;
  transition: opacity 0.3s;
}

.footer-politic,
.agree {
  margin: 0 10px;
}

.footer-politic:hover,
.agree:hover {
  opacity: 0.8;
}

/* Адаптивность */
@media (max-width: 1200px) {
  .footer-container {
    padding-inline: 40px;
  }
}

@media (max-width: 992px) {
  .footer-container {
    grid-template-columns: 1fr 1fr;
    grid-template-areas:
      "logo links"
      "info button"
      "bottom bottom";
    gap: 30px;
  }
  
  .footer-but {
    justify-content: flex-start;
    margin-top: 0;
  }
  
  .button-group {
    width: 100%;
    flex-wrap: wrap;
    justify-content: flex-start;
    align-items: start;
    gap: 15px;
    padding-top: 30px;
  }
  .footer-info{
    margin-top: 0;
  }
}

@media (max-width: 768px) {
  .footer-container {
    padding-inline: 16px;
    grid-template-columns: 1fr;
    grid-template-areas:
      "logo"
      "links"
      "info"
      "button"
      "bottom";
    max-width: 400px; /* Ограничиваем ширину контейнера */
    margin: 0 auto; /* Центрируем контейнер */
  }
  
  .logo-icon-footer {
    justify-content: center;
    justify-content: flex-start;
    margin-top: 20px;
    padding-left: 20px;
  }
  
  .footer-links,
  .footer-info {
    display: flex;
    flex-direction: column;
    align-items: flex-start; /* Выравниваем текст по левому краю */
    width: 100%;
    margin-top: 20px;
    padding: 0 20px; /* Добавляем отступы по бокам */
  }
  
  .footer-links {
    gap: 15px;
  }
  
  .footer-info {
    gap: 15px;
  }
  
  .footer-but {
    justify-content: center;
    justify-content: flex-start;
    margin: 20px 0;
    width: 100%;
  }
  
  .button-group {
    display: flex;
    flex-direction: column;
    justify-content: start;
    
    gap: 10px;
    padding-top: 20px;
    width: 100%;
  }
  
  .footer-politic,
  .agree {
    margin: 5px 0;
    display: flex;
    justify-content: start;

  }
}

@media (max-width: 480px) {
  .footer-container {
    padding-inline: 15px;
  }
  
  .telephone-group {
    align-items: center;
  }
  
  .footer-links a,
  .number-phone-footer,
  .email-info,
  .adress-info {
    font-size: 14px;
  }
  
  .button-group {
    font-size: 12px;
  }
}
</style>