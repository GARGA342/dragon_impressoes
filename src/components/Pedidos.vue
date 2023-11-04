<template>
    <section class="main">
        <h1>Pedidos</h1>
        <div class="content">
            <div class="social">
                <img src="../assets/img/wpp.svg"/>
                <img src="../assets/img/fb.svg"/>
                <img src="../assets/img/in.svg"/>
                <img src="../assets/img/insta.svg"/>
            </div>
            <div class="float_imgs">
                <img id="f_img1" src="../assets/img/float_image2.png"/>
                <img id="f_img2" src="../assets/img/float_image1.png"/>
                <img id="f_img3" src="../assets/img/float_image3.png"/>
            </div>
        </div>
    </section>
</template>

<style scoped>
    .main{
        background: #484848;
        padding: 5.62rem 0 0 0;
        height: 100vh;
    }

    .content{
        display: flex;
    }

    .social{
        display: flex;
        margin-top: 3.5rem;
        margin-left: 12rem;
        max-width: 500px;
        background: #484848;
        flex-direction: column;
        gap: 2rem;
    }

    .social img{
        width: 5.5rem;
        height: 5.5rem;
        cursor: pointer;
    }

    .float_imgs{
        display: flex;
        z-index: 0;
        margin-top: 80px;
    }

    .float_imgs img{
        position: absolute;
        max-width: 400px;
    }

    #f_img1{
        right: 30rem;
        margin-top: 12rem;
    }

    #f_img2{
        right: 25rem;
        margin-top: -7rem;
    }

    #f_img3{
        right: 2rem;
        margin-top: 3rem;
    }

    h1{
        color: white;
        font-weight: bold;
        margin-inline: 4.69rem;
    }
</style>