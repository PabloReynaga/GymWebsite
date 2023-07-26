<script>
  
import Contact from '..//routes/sections/contact/+page.svelte'
let y;

$:innerHeight= 0;
$:firstScreen = innerHeight-90;
$:secondScrenn= firstScreen + firstScreen;
$:thirdScreen= secondScrenn + firstScreen;
$:console.log(innerHeight-70)

$:console.log(y)

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

<svelte:window bind:scrollY={y} bind:innerHeight={innerHeight}/>
<header>

    <a href="#home"  class="logo">LOGO</a>
    

    <nav class="items-nav">
        <a href="#home" class:active={colored.homeButton} on:click={()=>{colored.homeButton=true, colored.aboutButton = false, colored.vlogButton = false, colored.contactMeButton= false}}>Home</a>
        <a href="#about" class:active={colored.aboutButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = true, colored.vlogButton = false, colored.contactMeButton= false}}>About</a>
        <a href="#vlog" class:active={colored.vlogButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = false, colored.vlogButton = true, colored.contactMeButton= false}}>Vlog</a>
        <a href="#contact" class:active={colored.contactMeButton} on:click={()=>{colored.homeButton=false, colored.aboutButton = false, colored.vlogButton = false, colored.contactMeButton= true}}>Contact me</a>
    </nav>

</header>
<body>
    
    <section id="home">
        <img alt="img"  src="../main-icon.png">
      home
    </section>
    <section id="about">about</section>
    <section id="vlog">vlog</section>
    <section id="contact" >
        <Contact/>
    </section>
</body>
<footer>
    <div class="footer">
        © Cacho Fitness Coach. All the right reserved. 2023 
    </div>
    
</footer>
<style lang="scss">

.footer{
    font-size: 10px;
    background-color: $bg-dark-gray;
    color: $secondary;
    padding: 10px;
    
}
    
.logo{
    font-size: 25px;
    text-decoration: none;
    color: $secondary ;
  
}
.active{
    color: $primary;
}


</style>