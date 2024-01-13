<script>
import Home from './..//routes/sections/home/+page.svelte'    
import Contact from '..//routes/sections/contact/+page.svelte'
import About from '../routes/sections/about/+page.svelte'
import Vlog from '../routes/sections/vlog/+page.svelte'
import icon from '$lib/icon/main-icon.png'
import MenuResponsive from '../componets/menuResponsive.svelte';
import './../index.css'
    
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
    <a href="#home">
        <img class="icon" alt="img" src={icon}/> 
    </a>

    {#if windowsWidth>650}
    <nav>
        <a href="#home" class:active={colored.homeButton} on:click={()=>{colored.homeButton=true, colored.aboutButton = false, colored.vlogButton = false, colored.contactMeButton= false}}>Inicio</a>
        <a href="#about" class:active={colored.aboutButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = true, colored.vlogButton = false, colored.contactMeButton= false}}>Transformación</a>
        <a href="#vlog" class:active={colored.vlogButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = false, colored.vlogButton = true, colored.contactMeButton= false}}>Mi Misión</a>
        <a href="#contact" class:active={colored.contactMeButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = false, colored.vlogButton = false, colored.contactMeButton= true}}>Contacto</a> 
    </nav>
    {/if}


    {#if windowsWidth<650}
    <div class="responsive-menu">
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
        <About/>
    </section>
    
    <section id="vlog">
        <Vlog/>
    </section>
    
    <section id="contact" >
        <Contact/>
    </section>

    <div class="focus-lost">


    </div>

</body>

<style lang="scss">

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
    height: 35px;
    transform: scale(2);
    object-fit: cover;
    margin-left: 10px;
    margin-top: 10px;
}


@media only screen and (max-width:650px){
nav a{
    display: none;
}

}
.focus-lost{
    background-color: red;
    height: 30%;
    width: 100%;
    position: fixed;

}
.responsive-menu{
    min-height: 100%;
}

</style>