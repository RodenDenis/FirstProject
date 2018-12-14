<template>
    <div class="navbar-container">
        <div class="navbar">
            <ul class="navbar-menu-left">
                <li class="navbar-item">Резюме</li>
                <li class="navbar-item">Вакансии</li>
                <li class="navbar-item">Компании</li>
                <li class="navbar-item">Услуги</li>
                <li class="navbar-item">Помощь</li>
                <li class="navbar-item">Проекты</li> 
            </ul>
            <ul class="empty-slot"></ul>
            <ul class="navbar-menu-rigth"></ul>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>
<style>
.navbar-container {
    height: 40px;
    width: 100%;
    background-color: black;
    color: white;
}
.navbar {
    width: 1320px;
    margin-left: 8%;
    display: grid;
    grid-template-columns: 3fr 2fr 2fr;
}
.navbar-menu-left {
    padding: 0px;
    text-align: center;
    margin: 0px;
    padding-left: 10px;
    display: flex;
    line-height: 40px;
}
.navbar-menu-rigth {
    line-height: 40px;
    padding: 0px;
    text-align: center;
    margin: 0px;
}
.navbar li {
    padding-right: 15px;
    padding-left: 15px;
    list-style-type: none;
    
}
.navbar li:hover {
    background-color: red;
}
</style>
