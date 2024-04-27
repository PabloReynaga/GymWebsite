<script>
import Logo from '$lib/icon/main-icon.png'
import IconInstgram from '$lib/icon/instagram-black.png'
import IconYoutube from '$lib/icon/youtube-black.png'

</script>

<div class="main">
    <div class="icon-container">
        <img alt="img" src={Logo} class="icon">
    </div>
    <div class="text-container">
        <p>© Copyright 2024. Cacholofitness. Todos los derechos reservados. Developed by Foreach.</p>
    </div>
    <div class="icon-social-media">
            <img alt="img" src={IconInstgram} class="icon-instagram">
            <img alt="img" src={IconYoutube} class="icon-youtube">
    </div>
    <div class="anchor-container">
        <a class="term-condition" href="/terms-conditions">Terminos y condiciones</a>
        <a class="term-condition" href="/#home">Volver al inicio</a>
        
    </div>
    
    
    

</div>
<style lang="scss">
    @import './../../../variables.scss';
    .main{
        height: 50vh;
        display: block;
        justify-content: center;
        color: $bg-bright;
        padding: 10%;
        
    }
    .icon-container{
        display: flex;
        justify-content: center;
        margin-bottom: 10px;
    }
    .icon{
        height: 80px;
    }
    .text-container{
        text-align: center;
        font-size: 15px;
    }
    .icon-instagram{
        height: 40px;
    }
    .icon-youtube{
        height: 43px;
        margin-left: 10px;
    }
    .icon-social-media{
        display: flex;
        justify-content: center;
        padding-top: 15px;
        
    }
    .anchor-container{
        display: block;
        width: 100%;
        justify-content: center;
        text-align: center;
        padding: 10px;
      
    }
   .term-condition{
    display: block;
    padding: 5px;
   }
</style>