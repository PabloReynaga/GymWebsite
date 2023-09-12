<script>
    import Button from './../../../componets/button.svelte'
    import Mainlogo from '$lib/icon/main-icon.png'
    $:responsiveMargin /= 20;
    $:responsiveMarginVar= responsiveMargin;

</script>
<svelte:window bind:innerHeight={responsiveMargin}/>
<div class="container">
   <div class="formular">
            
            <div class="container-input">
                <div class="header-titulos">
                    <h1 style="margin-top: {responsiveMarginVar}px" class="title">Conviertete en tu mejor versión!</h1>
                    <p class="p">Si te quedaron dudas contactame para ver tu situación y personalizar un plan específico para ti.</p>
                </div>
                
                <form action="https://formsubmit.co/Cacholofitness@gmail.com" method="post">
                    
                <label class="label-input"  for="name">Nombre*</label>
                <input class="input-field-name" type="text" id="name" required name="Nombre" autocomplete="off">
            
                <label class="label-input" for="mail">Mail*</label>
                <input class="input-field-mail" type="mail" id="mail" required name="Mail" autocomplete="off">
            
                <label class="label-input" for="number">Whatsapp*</label>
                <input class="input-field-phone" type="text" id="number" required name="Whatsapp" autocomplete="off">

                <label class="label-input" for="instagram">Instagram</label>
                <input class="input-field-instagram" type="text" id="instagram" name="Instagram" autocomplete="off">
    
                <label class="label-input" for="massage">Cuál es tu duda?</label>
                <textarea class="text-area-field" type="text" id="massage" name="Mensaje"
                >Hola! mi nombre es... y quiero empezar! </textarea>
                <div class="button-container">
                    <Button buttonValue="Enviar" img={Mainlogo}></Button>
                </div> 
                </form>
                
            </div>

         </div>
            

</div>


<style lang="scss">
    

*{
    font-size: 20px;
    margin: 0px;
    padding: 0px;
    font-family: 'Montserrat', sans-serif;
    
}


.formular{
    min-height: 80vh;
    display:block;
    justify-content: center;
    min-width: 80vw;

}
.container-input{
    display: block;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
    align-items: center;
}

.input-field-name{
    justify-content: center;
    display:flex;
    text-align: left;
    box-sizing: border-box;
    padding: 8px;
    margin: auto;
    color: $bg-dark;
    background-image: url(../../../lib/icon/avatar.png);
    background-repeat: no-repeat;
    padding-left: 40px;
    background-size: 30px;
    background-position: left;
    background-position-x: 3px;
    background-color: #3a3a3b;
}
.input-field-name:focus{
    outline: none;
    box-shadow:0px 0px 1px 1px $primary;
}
.input-field-mail{
    justify-content: center;
    display:flex;
    text-align: left;
    box-sizing: border-box;
    padding: 8px;
    margin: auto;
    color: $bg-dark;
    background-image: url(../../../lib/icon/sobre.png);
    background-repeat: no-repeat;
    padding-left: 40px;
    background-size: 30px;
    background-position: left;
    background-position-x: 5px;
    background-color: #3a3a3b;
    
}
.input-field-mail:focus{
    outline: none;
    box-shadow:0px 0px 1px 1px $primary;
}
.input-field-phone{
    justify-content: center;
    display:flex;
    text-align: left;
    box-sizing: border-box;
    padding: 8px;
    margin: auto;
    color: $bg-dark;
    background-image: url(../../../lib/icon/llamada-telefonica.png);
    background-repeat: no-repeat;
    padding-left: 40px;
    background-size: 30px;
    background-position: left;
    background-position-x: 5px;
    background-color: #3a3a3b;
    
}
.input-field-phone:focus{
    outline: none;
    box-shadow:0px 0px 1px 1px $primary;
}
.input-field-instagram{
    justify-content: center;
    display:flex;
    text-align: left;
    box-sizing: border-box;
    padding: 8px;
    margin: auto;
    color: $bg-dark;
    background-image: url(../../../lib/icon/compartir.png);
    background-repeat: no-repeat;
    padding-left: 40px;
    background-size: 30px;
    background-position: left;
    background-position-x: 5px;
    background-color: #3a3a3b;
    
}
.input-field-instagram:focus{
    outline: none;
    box-shadow:0px 0px 1px 1px $primary;
}
.label-input{
    justify-content: center;
    display: flex;
    margin: 20px;
    color: $secondary;
}
.title{
    display: flex;
    justify-content: center;
    font-size: 32px;
    padding: 10px;
    box-sizing: border-box;
    color: $secondary;
    
    
}
.p{
    display: flex;
    justify-content: center;
    padding: 25px;
    box-sizing: border-box;
    margin: auto;
}

.text-area-field{
    display: block;
    justify-content: center;
    align-items: center;
    margin: auto;
    resize: none;
    width: 297px;
    height: 15vh;
    padding: 8px;
    box-sizing: content-box;
    color: $bg-dark;
    background-color: #3a3a3b;
      
}

.text-area-field:focus{
    outline: none;
    box-shadow:0px 0px 1px 1px $primary;
}
.button-container{
    margin-bottom: 15px;
    padding-bottom: 10px;
}
.header-titulos{
    display: block;
    justify-content: center;
    margin-top: 60px;
   
}
.p{
    display: flex;
    justify-content: center;
}
</style>