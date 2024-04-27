<script>
import Home from './../routes/sections/home/+page.svelte'    
import Beneficios from '..//routes/sections/beneficios/+page.svelte'
import QueObtienes from '../routes/sections/queObtienes/+page.svelte'
import Alimentacion from '../routes/sections/alimentacion/+page.svelte'
import MiHistoria from '../routes/sections/miHistoria/+page.svelte/'
import Oferta from '../routes/sections/oferta/+page.svelte/'
import Preguntas from '../routes/sections/preguntas/+page.svelte/'
import Footer from '../routes/sections/footer/+page.svelte/'
import icon from './../lib/icon/main-icon.png'
import MenuResponsive from '../componets/menuResponsive.svelte';
import './../index.css'
import gsap from 'gsap'
  import { onMount } from 'svelte';

let animationIcon;
let animationResponsiveMenuButton;

onMount(()=>{
    
   
})
    
let y;
$:windowsWidth=0;
$:innerHeight= 0;
$:firstScreen = innerHeight-90;
$:secondScrenn= firstScreen + firstScreen;
$:thirdScreen= secondScrenn + firstScreen;
$: colored = {
    homeButton : true, 
    aboutButton :false,
    vlogButton:false, 
    contactMeButton : false
}

setInterval(()=>{
        switch(true){
        case firstScreen>y:
            colored.homeButton = true;
            colored.aboutButton= false;
            colored.vlogButton = false
            colored.contactMeButton =false;
            break;
        case firstScreen<y && secondScrenn>y:
            colored.homeButton= false;
            colored.aboutButton= true;
            colored.vlogButton= false;
            colored.contactMeButton=false;
            break;
        case secondScrenn<y && thirdScreen>y:
            colored.homeButton=false
            colored.aboutButton= false;
            colored.vlogButton= true;
            colored.contactMeButton=false
            break;
        case thirdScreen<y:
            colored.homeButton = false;
            colored.aboutButton= false;
            colored.vlogButton= false;
            colored.contactMeButton=true;
            break;
    } 
},10)

</script>

<svelte:window bind:scrollY={y} bind:innerHeight={innerHeight} bind:innerWidth={windowsWidth}/>
<header>
    <!-- <a href="#home">
        <img class="icon" alt="img" src={icon}
        bind:this={animationIcon}/> 
    </a> -->

    {#if windowsWidth>650}
    <nav>
        <a href="#home" class:active={colored.homeButton} on:click={()=>{colored.homeButton=true, colored.aboutButton = false, colored.vlogButton = false, colored.contactMeButton= false}}>Inicio</a>
        <a href="#about" class:active={colored.aboutButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = true, colored.vlogButton = false, colored.contactMeButton= false}}>Transformación</a>
        <a href="#vlog" class:active={colored.vlogButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = false, colored.vlogButton = true, colored.contactMeButton= false}}>Mi Misión</a>
        <a href="#contact" class:active={colored.contactMeButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = false, colored.vlogButton = false, colored.contactMeButton= true}}>Contacto</a> 
    </nav>
    {/if}


    {#if windowsWidth<650}
    <div class="responsive-menu" bind:this={animationResponsiveMenuButton}>
        <MenuResponsive>
            
        </MenuResponsive>
        
    </div>
    
    {/if}
    

</header>
<body>
    
    <section id="home">
        <Home/>
    </section>

    <section id="about">
        <QueObtienes/>
    </section>
    
    <section id="vlog">
        <Alimentacion/>
    </section>
    
    <section id="contact" >
        <Beneficios/>
    </section>

    <section id="" >
        <MiHistoria/>
    </section>

    <section id="" >
        <Oferta/>
    </section>

    <section id="" >
        <Preguntas/>
    </section>


</body>
<footer>
    <Footer/>
</footer>

<style lang="scss">
    @import '../variables.scss';

.footer{
    font-size: 10px;
    background-color: $bg-dark-gray;
    color: $secondary;
    padding: 10px;
    
}
    
.active{
    color: $primary;
}
.icon{
    height: 80px;
    object-fit: cover;
    animation-name: animationIcon;
    animation-duration: .5s;
}
.responsive-menu{
    animation-name: animationMenuButton;
    animation-duration: .5s;
}
@keyframes animationMenuButton {
  from {
    transform: translateX(100px);
  }

  to {
    transform: translateX(0px);
  }
}
@keyframes animationIcon {
  from {
    transform: translateX(-100px);
  }

  to {
    transform: translateX(0px);
  }
}


@media only screen and (max-width:650px){
nav a{
    display: none;
}

}
.focus-lost{
    
    height: 30%;
    width: 100%;
    position: fixed;

}
.responsive-menu{
    min-height: 100%;
}

</style>