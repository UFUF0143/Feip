<template>
  <header>
    <div class="header-block">
      <div class="header-group">
        <div class="logo-icon">
          <Logo />
        </div>
        <nav class="header-links">
          <a href="#" class="mobile-link">Реализованные проекты</a>
          <a href="#" class="mobile-link">Новости</a>
          <a href="#" class="mobile-link">Контакты</a>
        </nav>
      </div>
      
      <div class="number-cont">
        <img class="telephone" src="/image/telephone.png" alt="telephone">
        <span class="number-phone">+7 (900) 900-90-90</span>
        <Button class="desktop-btn">Оставить заявку</Button>
        
        <!-- Кнопка бургер-меню -->
        <button class="mobile-menu-btn" @click="toggleMenu">
          <img v-if="!isMenuOpen" src="/image/Button.png" alt="Меню">
          <img v-else src="/image/close.png" alt="Закрыть">
        </button>
      </div>
    </div>
      
      <!-- Мобильное меню -->
      <div class="mobile-menu" :class="{ 'active': isMenuOpen }">
        <div class="mobile-menu-content">
          <a href="#" class="mobile-link">Реализованные проекты</a>
          <a href="#" class="mobile-link">Новости</a>
          <a href="#" class="mobile-link">Контакты</a>
          <div class="footer-info-menu">
            <div class="telephone-group">
            <img class="telephone-footer" src="/image/telephone white.png" alt="telephone">
             <span class="number-phone-footer">+7 (900) 900-90-90</span></div>

             <div class="telephone-group">
                <img class="email" src="/image/email white.png" alt="email"> 
             <span class="email-info">info@gmail.com</span></div>
             
             <div class="telephone-group">
             <img class="adress" src="/image/adress white.png" alt="adress">
             <span class="adress-info">г. Владивосток<br>ул. Выселковая 49, стр. 3</span></div>

        </div>
        </div>
      </div>
    </header>
  </template>
  
  <script>
  export default {
  data() {
    return {
      isMenuOpen: false
    }
  },
  methods: {
  toggleMenu() {
    this.isMenuOpen = !this.isMenuOpen;
    // Блокировка прокрутки страницы при открытом меню
    document.body.style.overflow = this.isMenuOpen ? 'hidden' : 'visible';
  }
}
}
  </script>
  
  <style>
  .header-block {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: 24px 88px;
  }
  
  .header-group {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  
  .number-phone {
    font-family: Monserrat, sans-serif;
    font-size: 14px;
    white-space: nowrap;
    padding: 0 24px 0 8px;
    color: rgba(102, 102, 102, 1);
  }
  
  .header-links {
    font-family: Open Sans, sans-serif;
    font-size: 16px;
    display: flex;
    flex-wrap: wrap;
    gap: 24px;
    margin-left: 80px;
    margin-right: 40px;
    width: 100%;
  }
  .mobile-menu-content{
    font-family: Open Sans, sans-serif;
    font-size: 16px;
  }
  .mobile-menu-content {
    color: white;
    font-size: 18px;
  }

  .mobile-link{
    text-decoration: none;
    color: rgba(102, 102, 102, 1);
  }
  
  .number-cont {
    display: flex;
    align-items: baseline;
  }
  
  /* Стили для мобильного меню */
  .mobile-menu-btn {
    display: none;
    flex-direction: column;
    justify-content: space-between;
    width: 30px;
    height: 20px;
    background: transparent;
    border: none;
    cursor: pointer;
    padding: 0;
    z-index: 99999;
    
  }
  
  .mobile-menu-btn span {
    display: block;
    width: 100%;
    height: 2px;
    background: #666;
    transition: all 0.3s;
  }
  
  .mobile-menu {
    position: fixed;
    top: 0;
    right: -100%;
    width: 300px;
    height: 100vh;
    background: white;
    box-shadow: -5px 0 15px rgba(0,0,0,0.1);
    transition: right 0.3s ease;
    z-index: 1000;
    padding: 20px;
  }
  
  .mobile-menu.active {
    background: rgba(2, 159, 89, 1);
    right: 0;
  }
  
  .mobile-menu-content {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-top: 105px;
  }
  
  .desktop-btn {
    display: block;
  }
  .telephone{
    display: flex;
    align-items: center;
  }
  .footer-info-menu{
    margin-top: 378px;
    display: flex;
    flex-direction: column;
    gap: 24px;
    color: white;
    font-family: Monserrat, sans-serif;
    font-size: 14px;

  }


  /* Адаптация под 1010px */
  @media (max-width: 1010px) {
    .mobile-menu-btn {
    display: block;
  }
    .header-block {
      padding: 24px 20px;
    }
    
    .header-links {
      display: none;
    }
    
    .desktop-btn {
      display: none;
    }
    
    .mobile-menu-btn {
      display: flex;
      margin-left: 20px;
    }
    
    .number-cont {
      display: flex;
      align-items: center;
    }
  }
  @media (max-width: 510px) {
    .number-phone, .telephone{
        display: none;
    }
  }
  </style>