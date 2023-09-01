<script>
    import GymImgPerson from '$lib/img/gym-person.png'
    import GymImg from '$lib/img/gym.png'

</script>
<div>
    <h1 class="title">Mi Mision</h1>
    <div class="mision-container">
        <div class="first-container">
            <p class="first-text">Me converti en fitness-coach y cambie mi realidad.
                Ahora yo te guiaré para que tu puedas cambies la tuya.
            </p>
            <img class="first-img" alt="img" src={GymImgPerson}>
        </div>
        <div class="second-container">
            <img class="second-img" alt="img" src={GymImg}>
            <p class="second-text">Yo hare que tu esfuerzo y dedicacion de sus
                sus frutos y asi podras convertirte en el 
                gladeador que llevas dentro.
            </p>

        </div>
    </div>
</div>

<style lang="scss">
    *{
    font-size: 20px;
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

    }
    .first-container{
        display: flex;
        

    }
    .first-text{
        justify-content: center;
        display: flex;
        
        
    }
  
    .second-container{
        display: flex;

    }
    .second-text{
        padding: 5px;
        margin-left: 10px;
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
    
</style>