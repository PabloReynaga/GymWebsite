<script>
    import { onMount } from 'svelte';
    import Button from './../../../componets/button.svelte'
    import Logo from './../../../lib/icon/main-icon.png'
    import { gsap } from 'gsap'
    

let animationMainContainer;

onMount(()=>{
    gsap.from(animationMainContainer,{
        duration: 2,
         autoAlpha: 0,
         ease: "Power2.out"
    })
})

</script>
<div class="main-container" bind:this={animationMainContainer}>
    <div class="title-container">
        <h1  class="title">Bienvenido al team <span class="red-text">Cacholo Fitness!</span></h1>
        <p class="phase-title">Sé el primero en<span class="phase-title">cambiar la dirección de tu vida.</span></p>
        <div class="button-container " >
            <a href="https://form.jotform.com/233088635542056?fbclid=PAAaZD2cZsj6dzCI2gFxnQ45LCCAib_7hnK09gcX9B-kiiMbw-vSZwvDULe-I_aem_AQlXzsK5UPsVKqhcKewRfm0PK6efw21o0F9lwDP9cfOhityNw7S3Q3oHFbxsH8MgeZ0">
                <Button text="Comienza ahora!"></Button>
            </a>
    </div>
    </div> 
   
   
  
</div>
<style lang="scss">
    @import '../../../variables.scss';
*{
    font-size: 20px;
    margin: 0px;
    padding: 0px;
    font-family: 'Montserrat', sans-serif;
    
}
.title{
    position:relative;
    color: $secondary;
    font-size: 30px;
    text-align: center;
    font-weight: bold;
    text-transform: uppercase;
    

}
.red-text{
    font-size: 30px;
    color: $primary;
}

.button-container{
    display: block;
    bottom: 0;
    left: 0;
    right: 0;
    top: 10;
    z-index: 100;
    
}
.phase-title{
    text-transform: uppercase;
    font-size: 15px;
    padding-left: 2px;
    text-align: center;
    font-weight:10;
}

@media only screen and (width < 600px){
    .title-container{
    display: block;
    margin: auto;
    width: 100%;
    margin-top: 4rem;
    margin-bottom: 2rem;
    min-width: 4rem;
    padding-left:15px ;
    padding-right: 15px;
    background-color: $bg-dark-gray;
    
}
}
</style>