<script>
    import Img from '$lib/img/backGround.png'
    import Button from './../../../componets/button.svelte'
</script>
<body>
    
    <h1 class="titulo">Masteriza tu version superior</h1>
   
    <div class="img-container">
        <img class="img" alt="img" src={Img}>
    </div>    
    <div class="button-container" >
        <Button buttonValue="Let´s start"></Button>

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
    padding: 20px;
}
.img-container{
    border: red 5px;
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

</style>