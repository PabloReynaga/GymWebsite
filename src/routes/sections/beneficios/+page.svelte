<script>
    
    import InfoCard from '../../../componets/infoCard.svelte';
    import HomeIcon from '$lib/icon/home-icon.png' 
   

</script>




<div class="main-container">
    <div class="title-container">
        <p class="title">Beneficios <span style="color: #e21135;">exclusivos</span></p>
    </div>
    
    <div class="bonus-info-container">
        
        
            <InfoCard 
            title="✓ Entrenamiento en casa y gimnasio" 
            text="¡Entrena donde más te convenga! ¡Gimnasio o desde la comodidad de tu casa!"
            iconSorce={HomeIcon}
            iconSize = 40px
            backgroundColor = "black"
            background= "linear-gradient(rgba(29, 29, 29, 0.5), rgba(0, 0, 0, .7) 50%)"
            borderRadius = 30px
            border = "none"
            ></InfoCard>
            <InfoCard 
            title="✓ Entrenamiento en casa y gimnasio" 
            text="¡Entrena donde más te convenga! ¡Gimnasio o desde la comodidad de tu casa!"
            iconSorce={HomeIcon}
            iconSize = 40px
            background= "linear-gradient(rgba(29, 29, 29, 0.5), rgba(0, 0, 0, .7) 50%)"
            borderRadius = 30px
            border = "none"
            ></InfoCard>
            <InfoCard 
            title="✓ Entrenamiento en casa y gimnasio" 
            text="¡Entrena donde más te convenga! ¡Gimnasio o desde la comodidad de tu casa!"
            iconSorce={HomeIcon}
            iconSize = 40px
            backgroundColor = "red"
            borderRadius = 30px
            background= "linear-gradient(rgba(29, 29, 29, 0.5), rgba(0, 0, 0, .7) 50%)"
            border = "none"
            ></InfoCard>

       
    </div>
 
</div>
<style lang="scss">

@import '../../../variables.scss';
.main-container{
    background-color: $bg-dark-gray;
}
.title-container{
    margin: 20px;
}

.title{
    
    font-size: 25px;
    text-align: center;
    text-transform: uppercase;
    
    margin-bottom: 10px;

}
.bonus-info-container{
    
}

</style>