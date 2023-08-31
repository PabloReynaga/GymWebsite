<script>
    import Img from '$lib/img/backGround.png'
    import Button from './../../../componets/button.svelte'
    import IconWP from '$lib/icon/whatsapp.png'
</script>
<body>
    <h1 class="titulo">Masteriza tu version superior</h1>
    <div class="img-container">
        
        <img class="img" alt="img" src={Img}>
        
    </div>    
    <div class="button-container" >
        
            <a href="http://web.whatsapp.com/send?">
                <Button buttonValue="Let´s start" img={IconWP}></Button>
            </a>

    </div>
     
    
</body>
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
    
}
.test{
    background-color: white;
}
.iconWp{
    height: 200px;
}

</style>