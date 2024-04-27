<script>
    import { onMount } from 'svelte';
    import Button from './../../../componets/button.svelte'
    import { gsap } from 'gsap'
    

let animationMainContainer;
let animationLogo;
let animationMenuIcon;

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
        <h1  class="title">Bienvenido al team de <span class="red-text">Angel Lopez Fitness!</span></h1>
        <p class="phase-title">Sé el primero en<span class="phase-title">cambiar la dirección de tu vida.</span></p>
        <div class="button-container " >
            <a class="button" href="https://form.jotform.com/233088635542056?fbclid=PAAaZD2cZsj6dzCI2gFxnQ45LCCAib_7hnK09gcX9B-kiiMbw-vSZwvDULe-I_aem_AQlXzsK5UPsVKqhcKewRfm0PK6efw21o0F9lwDP9cfOhityNw7S3Q3oHFbxsH8MgeZ0">
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
.main-container{
    position: relative;
    min-height: 650px;
    min-width: 100%;
    background-image: url('../../../lib/img/main-photo.png');
    background-size:cover;
    background-position: center;
    background-repeat:no-repeat;
}
.title{
   display: block;
    color: $secondary;
    font-size: 30px;
    text-align: center;
    font-weight: bold;
    text-transform: uppercase;
    animation-name: animationFromLeft;
    animation-duration: .5s;
}
.red-text{
    font-size: 30px;
    color: $primary;
}

.button-container{
    z-index: 100;
    animation-name: animationFromRight;
    animation-duration: 1.5s;
    
    
}
.phase-title{
    text-transform: uppercase;
    font-size: 15px;
    padding-left: 2px;
    text-align: center;
    font-weight:10;
    margin-bottom: 15px;
    animation-name: animationFromLeft;
    animation-duration: 1s;
}
.title-container{
    position: absolute;
    margin: auto;
    bottom: 0;
    margin-bottom: 4rem;
    padding-left:15px ;
    padding-right: 15px;
    background-color: transparent;
}
.button{
    
}
@keyframes animationFromLeft{
    0%{
        transform: translateX(-200px);
    }
    100%{   
        transform: translateX(0px);
    }
}
@keyframes animationFromRight{
    0%{
        transform: translateX(300px);
    }
    100%{   
        transform: translateX(0px);
    }
}
</style>