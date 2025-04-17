<template>
    <header>
    <div class="header-block">
        <div class="header-group">
            <div class="logo-icon">
            <Logo />
        </div>
        <nav class="header-links">
                 <a href="#">Реализованные проекты</a>
                 <a href="#">Новости</a>
                 <a href="#">Контакты</a>
             </nav>
         </div>
         <div class="number-cont">
             <img class="telephone" src="/image/telephone.png" alt="telephone">
             <span class="number-phone">+7 (900) 900-90-90</span>

             <Button>Оставить заявку</Button>
         </div>
    </div>

    </header>
</template>
<style>

.header-block{
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
.number-phone{
    font-family: Monserrat, sans-serif;
    font-size: 14px;
    padding: 0 24px 0 8px;
    color: rgba(102, 102, 102, 1);
}
.header-links{
    font-family: Open Sans, sans-serif;
    font-size: 16px;
    display: flex;
    gap: 24px;
    margin-left: 80px;
    
}
a{
    text-decoration:none;
    color: rgba(102, 102, 102, 1);
}
</style>
