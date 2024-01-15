<script>
import { onMount} from 'svelte'

let svg = "<svg class='svg' xmlns='http://www.w3.org/2000/svg' height='45px' width='45px' viewBox='0 0 640 1792' style='background-color:inherit !important' fill='currentColor'> <path fill='inherit' d='M595 960q0 13-10 23l-466 466q-10 10-23 10t-23-10l-50-50q-10-10-10-23t10-23l393-393-393-393q-10-10-10-23t10-23l50-50q10-10 23-10t23 10l466 466q10 10 10 23z'></path> </svg>"
let buttonElements = [];

let preguntas = [ "¿Cómo recibo mi programa?","¿Es este un programa basado en suscripción?",
"¿El programa está disponible en todo el mundo?","¿Puedo hacer el plan en casa?"
,"Reembolsos y devoluciones.","¿Cómo cancelo?",
"Soy nuevo en el gimnasio, ¿es bueno para principiantes?","¿Todos los meses son iguales?"
]

onMount(()=>{
    buttonElements.forEach(button =>{
        button.innerHTML = svg;
    })
})

function handleClick(){

}

</script>

<div class="main-container">
    <div class="title-container">
        <h1 class="title">Preguntas frecuentes</h1>
    </div>
    <div class="preguntas-all-container">
    {#each preguntas as pregunta, i}
    <div class="pregunta-container">
        <button class="button" bind:this={buttonElements[i]} on:click={handleClick}></button>
        <p class="pregunta">{pregunta}</p>
    </div>
        
        
    
    {/each}
    </div>
</div>

<style lang="scss">
    @import '../../../variables.scss';
    .main-container{
        background-color: $bg-dark;
        
    }
    .title-container{
        width: 150px;
        justify-content: center;
        height: 100%;
        margin: auto;
       
        
    }
    .title{
        display: block;
        color: $bg-bright;
        font-size: 25px;
        justify-content: center;
        margin: auto;
        text-align: center;
        padding-top: 25px;
        
    }
    .pregunta{
        font-size:18px ;
        font-weight: lighter;
        text-align: left;
        transform: translateY(20%);
    }
    .button{
        width: 45px;
        height: auto;
        
    }
    .pregunta-container{
        display: flex;
        width: 100%;
        margin-top: 20px;
       
    }
    .preguntas-all-container{
        display: flex;
        width: 100%;
        height: auto;
        flex-wrap: wrap;
        padding: 40px;
        
    }
    .svg{
        background-color: red;
    }
</style>