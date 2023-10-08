<template>
    <div class="main" id="produtos">
        <h1>Produtos</h1>
        <div class="content">
            <div class="indicator"><img src="../assets/img/left_arrow.png" class="arrow"></div>

            <div class="card">
                <img src="../assets/img/cards/1.jpg" class="card_img" alt="">
                <p class="card_p">Porta copos de madeira</p>
                <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
            </div>

            <div class="card">
                <img src="../assets/img/cards/2.jpg" class="card_img" alt="">
                <p class="card_p">Artigos para decoração</p>
                <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
            </div>

            <div class="card">
                <img src="../assets/img/cards/3.jpg" class="card_img" alt="">
                <p class="card_p">Porta copos em PLA</p>
                <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
            </div>

            <div class="indicator"><img src="../assets/img/right_arrow.png" class="arrow"></div>
        </div>
    </div>
</template>

<style scoped>
    .main{
        background-color: #C50018;
        padding: 80px 0 80px 0;
    }

    h1{
        color: white;
        font-weight: bold;
        margin-inline: 4.69rem;
    }

    .content{
        margin-top: 1.5rem;
        height: 25rem;
        background: rgba(132, 0, 16, 0.28);
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    .card{
        width: 350px;
        height: 350px;
        border: 1px solid #484848;
        background: #FFF;
        box-shadow: 10px 10px 10px 10px rgba(0, 0, 0, 0.25);
    }

    .card_img{
        max-width: 300px;
        max-height: 250px;
        display: block;
        margin-inline: auto;
        margin-top: 10px;
        box-shadow: #484848 5px 5px 20px 1px;
    }

    .card_p{
        display: block;
        margin-top: 30px;
        margin-left: 2rem;
    }

    .arrow{
        height: 3rem;
        align-self: center;
    }

    .btn_pedido{
        display: block;
        border-radius: .8rem;
        background: #C50018;
        width: 90%;
        margin-inline: auto;
        margin-top: 15px;
        padding: .5rem;
        border: none;
        cursor: pointer;
    }

    .btn_pedido span{
        color: white;
        font-weight: 800;
        font-family: Inter;
    }   
</style>

<script setup>
</script>