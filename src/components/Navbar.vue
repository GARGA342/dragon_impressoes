<template>
    <div class="nav">
        <img src='../assets/img/nav_logo.png' width="49px" height="40px"/>
        <nav>
            <a href="#">Inicio</a>
            <a href="#">Produtos</a>
            <a href="#">Pedidos</a>
            <a href="#">Sobre</a>
        </nav>
    </div>
</template>

<style scoped>
.nav{
    background-color: #C50018;
    width: 100%;
    height: 4em;
    display: flex;
    /*box-shadow: 0px 2px 10px #000;*/
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
    align-items: center;
    justify-content: space-between;
}

nav{
    display: flex;
    margin-right: 20px;
    gap: 10px;
}

a{
    text-decoration: none;
    color: white;
    font-family: Inter;
}

a:hover{
    color:#FFAE03;
}

img{
    padding: 10px;
}
</style>
