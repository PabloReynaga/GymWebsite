<script>
    import Img from '$lib/img/backGround.png'
    import Button from './../../../componets/button.svelte'
    import Logo from './../../../lib/icon/main-icon.png'

$:responsiveMargin /= 20;
$:responsiveMarginVar= responsiveMargin;

</script>

<body>
    
    <h1 style="margin-top: {responsiveMarginVar}px" class="titulo">Masteriza tu versión superior</h1>
    <div class="img-container">

        <img class="img" alt="img" src={Img}>

    </div>    
    <div class="button-container " >
        
            <a href="https://wa.me/17670688111?text=Hola!%20Quiero%20empezar!">
                <Button buttonValue="Comienza ahora!" img={Logo} ></Button>
            </a>
    </div>
     
</body>
<svelte:window bind:innerHeight={responsiveMargin}/>
<style lang="scss">
*{
    font-size: 20px;
    margin: 0px;
    padding: 0px;
    font-family: 'Montserrat', sans-serif;
    
}
.titulo{
    display: flex;
    position:relative;
    color: $secondary;
    font-size: 25px;
    justify-content: center;
    text-align: center;
    width: auto;
    height: auto;
    box-sizing: border-box;
    top:70px;
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
*{
    background: $bg-dark;
}
.button-container{
    
    display: flex;
    justify-content: center;
    margin-bottom: 20px;
    margin-bottom: 15px;
    padding-bottom: 10px;
    
    
    
}



</style>