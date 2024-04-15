<script>

    import InfoCard from '../../../componets/infoCard.svelte';
   
    import HomeIcon from '$lib/icon/home-icon.png' 
    
    </script>
    <div class="img-alimentacion-container">
        
        <div class="manuernas-img-content-container">
            
            <p class="title-img-container">PLANES DE ALIMENTACIÓN PERSONALIZADOS</p>
            <p class="texto-img-container">Plan de comidas totalmente personalizado para TI Y TUS objetivos. Actualizado cada mes en función de tu progreso. ¡Elige entre comidas generales, vegetarianas, veganas y mucho más!</p>
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
    .img-alimentacion-container{
        position: block;
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
        
        font-size: 25px;
        text-align: center;
        text-transform: uppercase;
        color: $primary;
        margin-bottom: 10px;
    
    }
    .manuernas-img-content-container{
        display: block;
        top: 0;
        padding-top: 5%;
        padding-bottom: 5%;
        width: 100%;
        min-height: 100%;

        background-position: center;
        background-repeat: none;
        background-size:cover;
        backdrop-filter: blur(5px)
     
        
        
        
    }
    
    .subtitle-img-container{
        font-size: 3vh;
        text-align: center;
        text-transform: uppercase;
        margin-bottom: 10px;
        
    }
    .texto-img-container{
        font-size: 15px;
        text-align: center;
        text-transform: uppercase;
        
    }
    .info-cards{
        display: block;
       
        
    }
    .subtitle-img-container{
        text-align: center;
    }
    .img{
        width: 100%;
        height: auto;
    }
        
    </style>