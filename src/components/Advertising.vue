<template>
    <div class="advertising">
        <div class="advertising-info">
            тут будет твоя реклама
        </div>
        <div class="advertising-info">
            тут будет твоя реклама
        </div>
    </div>
</template>

<style>
.advertising {
    background-color: #f5f5f5;
    padding-top: 5px;
    min-height: 240px;
    max-height: 1200px;
    border-left: 1px solid #e7e7e7;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: repeat(5, 200px);
    text-align: center;
}
.advertising-info {
    width: 97%;
    height: 97%;
}
</style>
