<script>

import InfoCard from '../../../componets/infoCard.svelte';
import Phones from '$lib/img/phones-pictures.png'
import HomeIcon from '$lib/icon/home-icon.png' 

</script>
<div class="img-mancuernas-container">
    
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
            <img alt="img" class="img" src={Phones}>
        </div> 
    </div>
 
</div>
<style lang="scss">
    @import '../../../variables.scss';
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
    height: 100%;
}
.img-mancuernas{
    position: absolute;
    left: 0;
    top:0;
    width: 100%;
    height: 100%;
    object-fit:cover;
    object-position: center;
    filter: opacity(.3);
    
}
.title-img-container{
    
    font-size: 3vh;
    text-align: center;
    text-transform: uppercase;
    margin-bottom: 10px;

}
.manuernas-img-content-container{
    display: block;
    top: 0;
    padding-top: 5%;
    padding-bottom: 5%;
    width: 100%;
    min-height: 100%;
    background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, .9) 100%), url("../../../lib/img/mancuernas.png") ;
    background-position: center;
    background-repeat: none;
    background-size:cover;
    backdrop-filter: blur(5px)
 
    
    
    
}

.subtitle-img-container{
    font-size: 25px;
    text-align: center;
    text-transform: uppercase;
    margin-bottom: 10px;
    color: $primary;
}
.texto-img-container{
    font-size: 15px;
    text-align: center;
    text-transform: uppercase;
    
}
.info-cards{
    display: block;
   
    
}

.img{
    width: 100%;
    height: auto;
}
    
</style>