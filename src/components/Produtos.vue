<template>
    <section class="main" id="produtos">
        <h1>Produtos</h1>
        <div class="gallery">
           <img src="../assets/img/left_arrow.png" class="arrow prev">
            
            <div class="content">
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

                <div class="card active">
                    <img src="../assets/img/cards/3.jpg" class="card_img" alt="">
                    <p class="card_p">Porta copos em PLA</p>
                    <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
                </div>

                <div class="card">
                    <img src="../assets/img/cards/4.jpg" class="card_img" alt="">
                    <p class="card_p">Acessórios em PLA</p>
                    <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
                </div>

                <div class="card">
                    <img src="../assets/img/cards/4.jpg" class="card_img" alt="">
                    <p class="card_p">Acessórios em PLA</p>
                    <button class="btn_pedido"><span>FAÇA SEU PEDIDO</span></button>
                </div>
            </div>

            <img src="../assets/img/right_arrow.png" class="arrow next">
        </div>
    </section>
</template>

<style scoped>
    .main{
        background-color: #C50018;
        padding: auto 0 auto;
        min-height: 80vh;
    }

    h1{
        color: white;
        font-weight: bold;
        margin-inline: 4.69rem;
    }

    .content{
        display: flex;
        justify-content: space-around;
        align-items: center;
        overflow: auto;
        gap: 100px;
        max-width: 1200px;
        margin-inline: auto;
        -ms-overflow-style: none;  /* IE and Edge */
        scrollbar-width: none;  /* Firefox */
    }

    /* Hide scrollbar for Chrome, Safari and Opera */
    .content::-webkit-scrollbar {
        display: none;
    }

    .gallery{
        margin-top: 2.3rem;
        background: rgba(132, 0, 16, 0.28);
        height: 25rem;
        display: flex;
        align-items: center;
        padding-inline: 2.3rem;
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
        cursor: pointer;
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
import { onMounted } from "vue";

onMounted(() => {
    const controls = document.querySelectorAll('.arrow')
    const items = document.querySelectorAll('.card')
    let current_item = 0
    const max_items = items.length

    controls.forEach(control => {
        control.addEventListener('click', () =>{
            const prev = control.classList.contains('prev')
            if(prev){
                current_item -= 1
            }else{
                current_item += 1
            }

            if(current_item >= max_items){
                current_item = 0
            }

            if(current_item < 0){
                current_item = max_items - 1
            }

        })
    })
})
</script>