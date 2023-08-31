<script>
    import Img from '$lib/img/foto_about.png'

</script>
<div class="section-container">
    <div class="header-container">
        <h1 class= "title">Mi trasformación</h1>
        <p class = "subtitle">Luego de enfoque y dedicacion, genere un plan
           de coach para lograr mi transformación fisica.
        </p>
    </div>
    <div>
        <img class="img" alt="img" src={Img}>
    </div>
    <p>
    </p>
    <button></button>
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
        padding: 10px;
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
 
</style>