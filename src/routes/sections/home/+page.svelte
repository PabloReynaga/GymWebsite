<script>
    import { onMount } from 'svelte';
    import Button from './../../../componets/button.svelte'
    import Logo from './../../../lib/icon/main-icon.png'
    import { gsap } from 'gsap'
    import imgMancuernas from '$lib/img/mancuernas.png'
    import InfoCard from '../../../componets/infoCard.svelte';
    import HomeIcon from '$lib/icon/home-icon.png' 

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
        
            <a href="https://wa.me/34695193268?text=Hola!%20Quiero%20empezar!">
                <Button buttonValue="Comienza ahora!" img={Logo} ></Button>
            </a>
    </div>
    </div> 
    <div class="img-mancuernas-container">
        <img alt="img" class="img-mancuernas" src={imgMancuernas}>
        <div class="manuernas-img-content-container">
            <p class="title-img-container">Qué optienes?</p>
            <p class="subtitle-img-container">Planes de entrenamiento personalizados</p>
            <p class="texto-img-container">¡Por fin un programa de entrenamiento diseñado para ti! ¡Todos los ejercicios serán demostrados en video por mí para que puedas realizarlos correctamente! Se sentirá como si estuviéramos trabajando en persona.</p>
            <div class="info-cards">
                <InfoCard 
                title="✓ Entrenamiento en casa y gimnasio" 
                text="¡Entrena donde más te convenga! ¡Gimnasio o desde la comodidad de tu casa!"
                iconSorce={HomeIcon}
                iconSize = 40px
                ></InfoCard>
                <InfoCard 
                title="✓ Entrenamiento en casa y gimnasio" 
                text="¡Entrena donde más te convenga! ¡Gimnasio o desde la comodidad de tu casa!"
                iconSorce={HomeIcon}
                iconSize = 40px
                ></InfoCard>
                <InfoCard 
                title="✓ Entrenamiento en casa y gimnasio" 
                text="¡Entrena donde más te convenga! ¡Gimnasio o desde la comodidad de tu casa!"
                iconSorce={HomeIcon}
                iconSize = 40px
                ></InfoCard>
                <div></div>
                <div></div>
            </div> 
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
    display: block;
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
.img{
  width: 100%;
  height: 100%;
  object-fit:cover;
  object-position: center;
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
    position: relative;
    text-transform: uppercase;
    font-size: 15px;
    padding-left: 2px;
    text-align: center;
    font-weight:10;
   
}
p{
    margin-left: 70px;
    margin-right: 70px;
}
.img-mancuernas-container{
    position: relative;
    width: 100%;
    height: 50%;
}
.img-mancuernas{
    display: block;
    height: 1200px;
    min-width: 100%;
    object-fit:cover;
    object-position: center;
    filter: opacity(.3);
    
}
.title-img-container{
    
    font-size: 25px;
    text-align: center;
    text-transform: uppercase;
    color: $primary;
    margin-bottom: 10px;

}
.manuernas-img-content-container{
    position: absolute;
    top: 0;
    margin-top: 5%;
    width: 100%;
    
}
.subtitle-img-container{
    font-size: 28px;
    text-align: center;
    text-transform: uppercase;
    
}
.texto-img-container{
    font-size: 15px;
    text-align: center;
    text-transform: uppercase;
    
}
.info-cards{
    position: relative;
    top: 0; 
    
}
.subtitle-img-container{
    text-align: center;
}
@media only screen and (width < 600px){
    .title-container{
    display: block;
    margin: auto;
    width: 100%;
    margin-top: 4rem;
    min-width: 4rem;
    padding-left:15px ;
    padding-right: 15px;
    background-color: $bg-dark-gray;
    
}

}

</style>