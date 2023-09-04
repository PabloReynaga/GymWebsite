<script>
    import GymImgPerson from '$lib/img/gym-person.png'
    import GymImg from '$lib/img/gym.png'
    import ChainLeft from '$lib/img/chain-left.png'
    import ChainRight from '$lib/img/chain-right.png'
    
    
$:windowsWidth = 0;
$:responsiveMargin /= 20
$:responsiveMarginVar= responsiveMargin

</script>
<svelte:window bind:innerWidth={windowsWidth} bind:innerHeight={responsiveMargin}/>
<div>
    <h1 style="margin-top: {responsiveMarginVar}px;" class="title">Mi Misión</h1>
    <div class="mision-container">
        <div class="first-container">
            <div class="text-chain-container">
                <p class="first-text">Me convertí en fitness-coach y cambié mi realidad.
                    Ahora yo te guiaré para que tú puedas cambies la tuya.
                </p>
                <div class="container-first-img">
                    {#if windowsWidth>389}
                    <img class="chain-left" alt="img" src={ChainLeft}>
                {/if}

                </div>
                
               
            </div>
           
            <img class="first-img" alt="img" src={GymImgPerson}>
        </div>
        <div class="second-container">
            <img class="second-img" alt="img" src={GymImg}>
          <div>
            <p class="second-text">Juntos lograremos que tu esfuerzo y dedicación de 
                sus frutos y así podrás convertirte en el 
                gladiador que llevas dentro.
            </p>
            <div class="container-second-img">
                {#if windowsWidth>389}
                <img class="chain-right" alt="img" src={ChainRight}>
                {/if}
                

            </div>
           
          </div>
         

         

        </div>
    </div>
</div>

<style lang="scss">
    *{
    font-size: 18px;
    margin: 0px;
    padding: 0px;
    font-family: 'Montserrat', sans-serif;
    color: #ffff;
    }
    .mision-container{
    display: block;
    justify-content: center;
    padding: 25px;
    box-sizing: border-box;
    margin: auto;
    max-width: 800px;

    }
    .title{
        display:flex;
        justify-content: center;
        font-size: 32px;
        padding: 10px;
        box-sizing: border-box;
        margin-top: 500px;

    }
    .first-container{
        display: flex;
        

    }
    .first-text{
        justify-content: center;
        display: flex;
        height: 50%;
        display: flex;
        align-items: center;
        
        
        
    }
  
    .second-container{
        display: flex;

    }
    .second-text{
        padding: 5px;
        margin-left: 10px;
        height: 60%;
        display: flex;
        align-items: center;
        margin-top: 15px;
    }
    .first-img{
        width: 50%;
    height: 50%;
    object-fit:cover;
    object-position: left;
  
    }
    .second-img{
    
    width: 50%;
    height: 50%;
    object-fit:cover;
    object-position: right;

    }
    .chain-left{
        width: 70%;
        height: 70%;
        display: block;
    margin-top: 10px;
        }
    .chain-right{
        width: 100%;
        height: 80%;
        display: flex;
        float: right;
      

    }   
    .container-first-img{
        height: 50%;
        display: flex;
        align-items: center;
    }
    .container-second-img{
        height: 30%;
        display: flex;
        justify-content: right;
        align-items: center;
        
    }
</style>