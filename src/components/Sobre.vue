<template>
    <section class="main" id="sobre">
        <h1>Sobre nós</h1>
        <div class="content">
            <!-- Primeiro bloco -->
            <p id="p1" class="l_transition">Lorem ipsum dolor sit amet, consectetur adipiscing elit. In id faucibus ligula. Donec posuere vestibulum lacinia. Phasellus ut magna orci. Maecenas vel magna in odio fermentum congue sit amet at nisi. Proin dignissim non orci id consequat. Curabitur et placerat augue, ut dignissim augue. Phasellus massa ligula, mollis quis lacus a, cursus lacinia risus. Phasellus eget nulla gravida, cursus est a, faucibus orci.</p>
            <img src="../assets/img/generic-1.png" class="r_transition" id="rimg">
            
            <!-- Paŕagrafo ao centro -->
            <p id="p2" class="l_transition">Lorem ipsum dolor sit amet, consectetur adipiscing elit. In id faucibus ligula. Donec posuere vestibulum lacinia. Phasellus ut magna orci. Maecenas vel magna in odio fermentum congue sit amet at nisi. Lorem ipsum dolor sit amet, consectetur adipiscing elit. In id faucibus ligula. Donec posuere vestibulum lacinia.</p>
           
            <!-- Último bloco -->
            <img src="../assets/img/generic-1.png" class="l_transition" id="limg">
            <p id="p3" class="r_transition">Proin dignissim non orci id consequat. Curabitur et placerat augue, ut dignissim augue. Phasellus massa ligula, mollis quis lacus a, cursus lacinia risus. Phasellus eget nulla gravida, cursus est a, faucibus orci. Donec maximus purus id metus interdum, vel commodo diam suscipit.</p>
        </div>
    </section>
</template>

<style scoped>
    .main{
        margin: auto 0 auto 4.69rem;
        min-height: 80vh;
        overflow-x: hidden;
    }

    .content{
        display: grid;
        gap: 20px;
        grid-template-columns: auto auto auto;
        max-width: 1200px;
        margin: 0 auto;
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

    .content img{
        max-width: 100%;
    }

    .main h1{
        color: #000;
        font-weight: bold;
        margin-bottom: 1.5rem;
    }

    .content p{
        font-size: large;
        max-width: 100%;
    }

    #div{
        display: block;
        width: 100%;
        background-color: white;
    }

    .l_transition{
        transform: translateX(-50%);
        transition: transform 1.7s ease;  
        opacity: 0;
    }

    .r_transition{
        transform: translateX(+50%);
        transition: transform 1.7s ease;
        opacity: 0;
    }

    .show{
        transform: translateX(0);

        animation: fadein 3s;
        -webkit-animation: fadein 3s; /* Safari, Chrome and Opera > 12.1 */
       -moz-animation: fadein 3s; /* Firefox < 16 */
        -ms-animation: fadein 3s; /* Internet Explorer */
         -o-animation: fadein 3s; /* Opera < 12.1 */
            animation: fadein 3s;
            opacity: 1;
    }

    @keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Firefox < 16 */
    @-moz-keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Safari, Chrome and Opera > 12.1 */
    @-webkit-keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Internet Explorer */
    @-ms-keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }

    /* Opera < 12.1 */
    @-o-keyframes fadein {
        from { opacity: 0; }
        to   { opacity: 1; }
    }
</style>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const l_elements = document.querySelectorAll('.l_transition')
  const r_elements = document.querySelectorAll('.r_transition')
  window.addEventListener('scroll', checkBoxes)

  function checkBoxes(){
    const triggerBottom = window.innerHeight / 5 * 4
    l_elements.forEach((box) => {
        const boxTop = box.getBoundingClientRect().top

        if(boxTop < triggerBottom){
            box.classList.add('show')
        }
    })

    r_elements.forEach((box) => {
        const boxTop = box.getBoundingClientRect().top

        if(boxTop < triggerBottom){
            box.classList.add('show')
        }
    })
  }
})
</script>