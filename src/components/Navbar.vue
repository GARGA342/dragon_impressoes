<template>
    <div class="nav_body">
        <a href="#inicio"><img src='../assets/img/nav_logo.png' class="nav_logo" alt="Logo da empresa"/></a>
        <nav class="nav_links">
            <a href="#inicio">Inicio</a>
            <a href="#home_div">Sobre</a>
            <a href="#about_div">Produtos</a>
            <a href="#pedidos">Pedidos</a>
        </nav>
    </div>
</template>

<style scoped>
.nav_body{
    position: fixed;
    background-color: #C50018;
    width: 100%;
    height: 4em;
    display: flex;
    /*box-shadow: 0px 2px 10px #000;*/
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
    align-items: center;
    justify-content: space-between;
    z-index: 1;
}

.nav_links{
    display: flex;
    margin-right: 20px;
    gap: 10px;
}

.nav_links a{
    text-decoration: none;
    color: white;
    font-family: Inter;
}

.nav_links a:hover{
    color:#FFAE03;
}

.nav_logo {
    padding: 10px;
    width: 50px;
    cursor: pointer;
}
</style>
