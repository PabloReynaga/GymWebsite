<script>
    import Img from '$lib/img/backGround.png'
    import Button from './../../../componets/button.svelte'
</script>
<body>
    
        <h1 class="titulo">Masteriza tu version superior</h1>
    <img class="img" alt="img" src={Img}>
    
    <div class="button-container" >
        <Button buttonValue="Let´s start"></Button>

    </div>
    
</body>
<style lang="scss">

.titulo{
    display: flex;
    justify-content: center;
    position:relative;
    color: $secondary;
    font-size: 40px;
    top: 130px;
    padding: 15px;
    
    
}

.img{
 width: 90%;
  height: 700px;
  object-fit: cover;
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