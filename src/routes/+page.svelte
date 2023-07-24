<script>
import Contact from '..//routes/sections/contact/+page.svelte'
let y=0;

$:innerHeight=0;

$: console.log(y);
$: console.log(innerHeight)
$: colored = {
    homeButton : true, 
    aboutButton :false,
    vlogButton:false, 
    contactMeButton : false}


</script>
<svelte:window bind:scrollY={y} bind:innerHeight />
<header>
    <a href="#home" class="logo">LOGO</a>      
    <nav class="items-nav">
        <a href="#home" class:active={colored.homeButton} on:click={()=>{colored.homeButton=true, colored.aboutButton = false, colored.vlogButton = false, colored.contactMeButton= false}}>Home</a>
        <a href="#about" class:active={colored.aboutButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = true, colored.vlogButton = false, colored.contactMeButton= false}}>About</a>
        <a href="#vlog" class:active={colored.vlogButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = false, colored.vlogButton = true, colored.contactMeButton= false}}>Vlog</a>
        <a href="#contact" class:active={colored.contactMeButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = false, colored.vlogButton = false, colored.contactMeButton= true}}>Contact me</a>
    </nav>
</header>
<body>
    <section id="home">
        <div class="home-container">Home

        </div>
    </section>
    <section id="about">about</section>
    <section id="vlog">vlog</section>
    <section id="contact" >
        <Contact/>

    </section>
</body>

<style lang="scss">
    
.logo{
    font-size: 25px;
    text-decoration: none;
    color: $secondary ;
  
}
.active{
    color: $primary;
}

.home-container{
    font-size: 27px;
}

</style>