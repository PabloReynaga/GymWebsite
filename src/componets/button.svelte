<script>
export let text;
export let width = undefined;
export let height = undefined;


</script>

    <div class="main-button" style="height: {height}; width:{width}">
        <button class="button-container" >
            <p class="button-text">{text}</p>
        </button>
    </div>

<style lang="scss">
    @import '../variables.scss';
.main-button {
    display: flex;
    font-size: 20px;
    margin-top: 10px;
    width: 250px;
    height: 50px;
    border: none;
    outline: none;
    color: #fff;
    background: #0000;
    cursor: pointer;
    position: relative;
    z-index: 0;
    margin: auto;
    
    
}

.main-button:active:after {
    background: transparent;
   background-color: $bg-dark;
  
}
.main-button:after {
    z-index: -1;
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: $primary;
    left: 0;
    top: 0;
    border-radius: 100px;
   
}
.button-container{
    display: flex;
    justify-content: center;
    text-align: center;
    width: 100%;
    height: auto;
    transform: translateY(15%);
    
    
    
    
    

}
.button-text{
    
    text-align: center;
}


</style>