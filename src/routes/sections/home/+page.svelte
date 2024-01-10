<script>
    import Img from '$lib/img/backGround.png'
    import { onMount } from 'svelte';
    import Button from './../../../componets/button.svelte'
    import Logo from './../../../lib/icon/main-icon.png'
    import { gsap } from 'gsap'

let animationMainContainer;

onMount(()=>{
    gsap.from(animationMainContainer,{
        duration: 1.5,
         autoAlpha: 0,
         ease: "Power2.out"
    })
})


</script>
<div class="main-container" bind:this={animationMainContainer}>
    <div class="title-container">
        <h1  class="title">Bienvenido al team <span class="red-text">Cacholo Fitness!</span></h1>
    </div>
    
    <div class="img-container">

        <img class="img" alt="img" src={Img}>

    </div>    
    <div class="button-container " >
        
            <a href="https://wa.me/34695193268?text=Hola!%20Quiero%20empezar!">
                <Button buttonValue="Comienza ahora!" img={Logo} ></Button>
            </a>
    </div>
</div>
<style lang="scss">
*{
    font-size: 20px;
    margin: 0px;
    padding: 0px;
    font-family: 'Montserrat', sans-serif;
    
}
.title{
    position:relative;
    color: $secondary;
    font-size: 27px;
    text-align: center;
    top:70px;
    font-weight: bold;

}
.red-text{
    font-size: 27px;
    color: $primary;
}
.img-container{
  
    display: flex;
    height: 600px;
}
.img{
  width: 100%;
  height: 100%;
  object-fit:cover;
  object-position: center;
}

.button-container{
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    top: 88%;
    justify-content: center;
    margin-bottom: -10px;
    padding-bottom: 10px;
    
    
    
}
.title-container{
    display: flex;
    margin: auto;
    max-width: 300px;
    padding-left:15px ;
    padding-right: 15px;
}


</style>