<template>
    <div class="header">
        <div class="header-container">
            <div class="logo">
                <a href="/" title="hh.ua">
                    <img src="/images/logo.svg" class="header-logo">
                    <img src="min-hh-red.png" class="header-zone">
                </a>
            </div>
            <div class="search">
                <form class="search-form" action="">
                    <input class="header-form-input" type="text" placeholder="Я ищу...">
                    
                    <select class="header-button button-gray">
                        <option value="" selected>Проекты</option>
                        <option value="">Пользователи</option>
                        <option value="">Инфо</option>
                    </select>
                </form>
                <button class="header-button button-blue">Найти</button>
            </div>
            <div class="header-menu">
                <ul class="header-list">
                    <li><a href="" class="header-list-btn">Показать все</a></li>
                    <li><a href="" class="header-list-btn">Предыдущий</a></li>
                    <li><a href="" class="header-list-btn">Следующий</a></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
.header {
    background: #f5f5f5;
    width: 100%;
    min-height: 78px;
    
}
.header-logo {
    height: 48px;
    width: 50px;
}
.header-zone {  
    height: 48px;
    width: 50px;
    
}
.header-list {
    padding-left: 0px;
}
.header-list li {
    display: inline;
}
.header-container {
    width: 1320px;
    margin-left: 7%;
    padding-top: 10px;
    display: grid;
    grid-template-columns: 1fr 6fr 2fr;
}
.header-list-btn {
    color: #999;
    margin-right: 15px;
    text-decoration: none;
}
.search-form {
    display: inline-block;
    width: 85%;
}
.header-form-input {
    width: 82%;
    height: 36px;
    padding: 0px;
    padding-left: 15px;
}
.header-button {
    height: 40px;
    width: 100px;
}
.search {
    padding-top: 6px;
}
.button-blue {
    margin: 0;
    border: none;
    overflow: visible;
    font: inherit;  
    display: inline-block;
    vertical-align: middle;
    font-size: 14px;
    line-height: 38px;
    text-align: center;
    text-transform: uppercase;
    background-color: #1e87f0;
    color: #fff;
    border: 1px solid transparent;
}
.button-gray {
    background-color: #f9f9f9;
}
</style>
