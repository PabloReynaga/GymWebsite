<script>
    import Img from '$lib/img/foto_about.png'
    import IconInstagram from '$lib/icon/instagram.png'
    import IconYouTube from '$lib/icon/youtube.png'
$:responsiveMargin /= 13;
$:responsiveMarginVar= responsiveMargin;
$:windowWidth = 0;
$: result = windowWidth> 500? "max-width: 70%;  max-height: 70%; ": " " ;
</script>
<svelte:window bind:innerHeight={responsiveMargin} bind:innerWidth={windowWidth}/>
<div class="section-container">
    <div class="header-container">
        <h1 style="margin-top: {responsiveMarginVar+15}px;" class= "title">Mi Transformación</h1>
        <p class = "subtitle">Con mucho enfoque y dedicación cree un plan
           para lograr un cambio real y duradero.
        </p>
    </div>
    <div class="img-container">
        <img style="{result}" class="img" alt="img" src={Img}>
    </div>
    <p class="redessociales">Sígueme en mis redes sociales 
        para poder ver más:
    </p>
    <div class="container-icons">
        <div class="container-icons-instagram">
            <a href="https://instagram.com/cacholofitness?igshid=MzRlODBiNWFlZA==">
                <button class="icon-instagram">
                    <img  alt="img" src={IconInstagram}>
                </button>
            </a>

        </div>
        <div class="container-icons-youtube">
            <a href="https://www.youtube.com/@CacholoFitness">
                <button class="icon-youtube">
                    <img  alt="img" src={IconYouTube}>
                </button>
            </a>
            

        </div>
      
       
        
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
        display: flex;
        justify-content: center;
        font-size: 32px;
        margin-top: 60px;
        box-sizing: border-box;
        color: $secondary;
       
       
    }
    .subtitle{
        display: flex;
    justify-content: center;
    padding: 25px;
    box-sizing: border-box;
    margin: auto;
    }
    .header-container{
        display: block;
        justify-content: center;
        align-items: center;
        
    }
    .img{
        padding: 20px;
        max-width: 100%;
        max-height: 100%;
        object-position: center;
        display: flex;
        justify-content: center;
        
    }
    .img-container{
        display: flex;
        justify-content: center;
        
      
      
    }
    .container-icons{
        display: flex;
        justify-content: center;
    }
    .icon-instagram{
        width: 50px;
        display: flex;
        justify-content: center;
        margin-right: 15px;
    }
    .icon-youtube{
        width: 55px;
        display: flex;
        justify-content: center;
        margin-right: 15px;
        margin-bottom: 20px;
    }
    .redessociales{
        display: flex;
    justify-content: center;
    padding: 25px;
    box-sizing: border-box;
    margin: auto;

    }
    .container-icons-instagram{
        width: 50%;
        height: 100px;
        display: flex;
        justify-content: right;
        margin-right: 20px;
    }
    .container-icons-youtube{
        width: 50%;
        height: 100px;
        display: flex;
        justify-content: left;
      
    }
</style>