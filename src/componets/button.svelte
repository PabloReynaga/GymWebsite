<script>

export let buttonValue;
export let img;


    
</script>

<main>
    <button class="main-button">
        <div class="button-container">
            <p class="button-text">{buttonValue}</p>
            <img class="iconWP" src={img}>

        </div>
        
        
    </button>
</main>

<style lang="scss">
.main-button {
    display: block;
    justify-content: center;
    font-size: 20px;
    margin: auto;
    margin-top: 25px;
    width: 220px;
    height: 50px;
    border: none;
    outline: none;
    color: #fff;
    background: $bg-dark;
    cursor: pointer;
    position: relative;
    z-index: 0;
}
.main-button:before {
    content: '';
    background: linear-gradient(45deg, $primary,  $primary);
    position: absolute;
    top: -2px;
    left:-2px;
    background-size: 400%;
    z-index: -1;
    filter: blur(5px);
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    animation: glowing 20s linear infinite;
    opacity: 0;
    transition: opacity .3s ease-in-out;
}

.main-button:active:after {
    background: transparent;
    
}

.main-button:hover:before {
    opacity: 1;
}

.main-button:after {
    z-index: -1;
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: #111;
    left: 0;
    top: 0;
   
}
.button-container{
    display: flex;
    justify-content: center;

}
.button-text{
    margin-left: 25px;
}
.iconWP{
    height: 30px;
    float: right;
    margin-left: 10px;
    display: flex;
    justify-content: center;
}

</style>