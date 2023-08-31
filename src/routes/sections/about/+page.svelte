<script>
    import Img from '$lib/img/foto_about.png'
    import IconInstagram from '$lib/icon/instagram.png'
    import IconYouTube from '$lib/icon/youtube.png'

</script>
<div class="section-container">
    <div class="header-container">
        <h1 class= "title">Mi trasformación</h1>
        <p class = "subtitle">Luego de enfoque y dedicacion cree un plan
           para lograr un cambio real y duradero en mi fisico.
        </p>
    </div>
    <div>
        <img class="img" alt="img" src={Img}>
    </div>
    <p class="redessociales">Sigueme en mi redes sociales 
        para poder ver más:
    </p>
    <div class="container-icons">
        <button class="icon-instagram">
            <img  alt="img" src={IconInstagram}>
        </button>
        <button class="icon-youtube">
            <img  alt="img" src={IconYouTube}>
        </button>
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
    }
    .container-icons{
        display: flex;
        justify-content: center;
    }
    .icon-instagram{
        width: 35px;
        display: flex;
        justify-content: center;
        margin-right: 15px;
    }
    .icon-youtube{
        width: 40px;
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
 
</style>