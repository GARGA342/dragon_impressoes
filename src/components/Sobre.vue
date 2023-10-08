<template>
    <div class="main">
        <h1>Sobre nós</h1>
        <div class="content">
            <!-- Primeiro bloco -->
            <p id="p1">Lorem ipsum dolor sit amet, consectetur adipiscing elit. In id faucibus ligula. Donec posuere vestibulum lacinia. Phasellus ut magna orci. Maecenas vel magna in odio fermentum congue sit amet at nisi. Proin dignissim non orci id consequat. Curabitur et placerat augue, ut dignissim augue. Phasellus massa ligula, mollis quis lacus a, cursus lacinia risus. Phasellus eget nulla gravida, cursus est a, faucibus orci.</p>
            <img src="../assets/img/generic-1.png" class="text_img" id="rimg">
            
            <!-- Paŕagrafo ao centro -->
            <p id="p2">Lorem ipsum dolor sit amet, consectetur adipiscing elit. In id faucibus ligula. Donec posuere vestibulum lacinia. Phasellus ut magna orci. Maecenas vel magna in odio fermentum congue sit amet at nisi. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In id faucibus ligula. Donec posuere vestibulum lacinia. Phasellus ut magna orci. Maecenas vel magna in odio fermentum congue sit amet at nisi. </p>
           
            <!-- Último bloco -->
            <img src="../assets/img/generic-1.png" class="text_img" id="limg">
            <p id="p3">Proin dignissim non orci id consequat. Curabitur et placerat augue, ut dignissim augue. Phasellus massa ligula, mollis quis lacus a, cursus lacinia risus. Phasellus eget nulla gravida, cursus est a, faucibus orci. Donec maximus purus id metus interdum, vel commodo diam suscipit.</p>
        </div>
    </div>
    <img src="../assets/img/red_div.png" id="div">
</template>

<style scoped>
    .main{
        margin-top: 30px;
        margin-inline: 4.69rem;
    }

    .content{
        display: grid;
        gap: 20px;
        grid-template-columns: auto auto auto;
    }

    #p1{
        grid-column-start: 1;
        grid-column-end: 3;
        grid-row-start: 1;
    }

    #p2{
        grid-column-start: 2;
        grid-row-start: 2;
    }

    #p3{
        grid-column-start: 2;
        grid-column-end: 4;
        grid-row-start: 3;
    }

    #rimg{
        grid-row-start: 1;
        grid-row-end: 3;
    }

    #limg{
        grid-row-start: 2;
        grid-row-end: 4;
    }

    .text_img{
        width: 400px;
    }

    h1{
        color: #000;
        font-weight: bold;
        margin-bottom: 1.5rem;
    }

    p{
        font-size: large;
    }

    #div{
        display: block;
        width: 100%;
        background-color: white;
    }
</style>
