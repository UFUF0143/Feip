<template>
    <footer>
        <div class="footer-group">
        <div class="logo-icon-footer">
            <LogoFooter />
        </div>

        <nav class="footer-links">
                 <a href="#">Реализованные проекты</a>
                 <a href="#">Новости</a>
                 <a href="#">Контакты</a>
             </nav>
        <div class="footer-info">
            <div class="telephone-group">
            <img class="telephone" src="/image/telephone.png" alt="telephone">
             <span class="number-phone-footer">+7 (900) 900-90-90</span></div>

             <div class="telephone-group">
                <img class="email" src="/image/email.png" alt="email"> 
             <span class="email-info">info@gmail.com</span></div>
             
             <div class="telephone-group">
             <img class="adress" src="/image/adress.png" alt="adress">
             <span class="adress-info">г. Владивосток<br>ул. Выселковая 49, стр. 3</span></div>

        </div>
        <div class="footer-but">
        <Button>Оставить заявку</Button>
    </div>
            </div>
            <div class="button-group">
            <p class="footer-link">© Загдом, 2021</p>
            <a class="footer-politic" href="#">Политика конфиденциальности</a>
            <a class="agree" href="#">Пользовательское соглашение</a>
        </div>
    </footer>
</template>

<style>
footer{
    background-color: rgba(37, 71, 65, 1);
}
.footer-group{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding-left: 88px;
    padding-right: 88px;
}
.logo-icon-footer{
    margin-top: 37px;
}
.footer-links{
    display: flex;
    gap: 24px;
    flex-direction: column;
    font-family: Open Sans, sans-serif;
    color: white;
    font-size: 16px;
    margin-top: 49px;

}
.footer-links a{
    font-family: Open Sans, sans-serif;
    color: white;
    font-size: 16px;
}
.footer-info{
    display: flex;
    flex-direction: column;
    gap: 24px;
    color: white;
    font-family: Monserrat, sans-serif;
    font-size: 14px;
    margin-top: 48px;

}
.footer-info .number-phone{
    color: white;
}
.footer-but{
    margin-top: 32px;
}
.footer-bottom-line{
    display: flex;
    flex-direction: row;
    font-family: Open Sans, sans-serif;
    color: white;
    font-size: 14px;
    margin-left: 88px;
    margin-right: 88px;
    padding-bottom: 33px;
}

.footer-links .footer-politic{
    margin-left: 6px;
    margin-top: 18px;
    font-size: 14px;
}
.footer-info .agree{
    color: white;
}

.number-phone-footer{
    font-family: Monserrat, sans-serif;
    font-size: 14px;
    margin-left: 8px;
}
.adress-info{
    font-family: Monserrat, sans-serif;
    font-size: 14px;
    margin-left: 8px;
}
.email-info{
    font-family: Monserrat, sans-serif;
    font-size: 14px;
    margin-left: 8px;
}
.button-group {
    display: flex;
    justify-content: space-between; 
    align-items: center; 
    margin-top: 32px;
    padding-left: 88px;
    padding-right: 88px;
    padding-bottom: 33px;
    width: 75%;
    opacity: 0.6;

}

.footer-link {
    font-family: Open Sans, sans-serif;
    color: white;
    font-size: 14px;
}

.footer-politic,
.agree {
    font-family: Open Sans, sans-serif;
    color: white;
    font-size: 14px;
}


</style>