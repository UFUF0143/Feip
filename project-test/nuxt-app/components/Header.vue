<template>
    <header>
    <div class="header-block">
        <div class="header-group">
            <div class="logo-icon">
            <Logo />
        </div>
        <nav>
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
    padding: 0 24px 0 8px;
    color: rgba(102, 102, 102, 1);
}
nav{
    display: flex;
    gap: 24px;
    margin-left: 80px;
    
}
a{
    text-decoration:none;
    color: rgba(102, 102, 102, 1);
}
</style>
