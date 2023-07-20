<script>
let y=0;

$:innerHeight=0

$: console.log(y);
$: console.log(innerHeight)
$: colored = ""


</script>
<svelte:window bind:scrollY={y} bind:innerHeight />
<header>
      

    <a href="#home" class="logo">LOGO</a>      
    <nav class="items-nav">
        
        <a href="#home" class="active" >Home</a>
        <a href="#about" class={colored}>About</a>
        <a href="#vlog" class={colored}>Vlog</a>
        <a href="#contact" class={colored}>Contact me</a>
    </nav>
    
    

</header>
<body>
    <section id="home">
        <div class="home-container">

        </div>
    </section>
    <section id="about">about</section>
    <section id="vlog">vlog</section>
    <section id="contact">contact</section>
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