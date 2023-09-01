<script>
    import Button from './../../../componets/button.svelte'
    import Pesa_icono from '$lib/icon/main-icon.png'

</script>
<div class="container">
   <div class="formular">
            
            <div class="container-input">
                <div class="header-titulos">
                    <h1 class="title">Trabajemos juntos en tus metas!</h1>
                    <p class="p">Si te quedaron dudas contactame para ver tu situacion y perzonalizar un plan especifico para ti.</p>
                </div>
                
                <form action="https://formsubmit.co/reynagafarias@gmail.com" method="post">
                    
                <label class="label-input"  for="name">Nombre*</label>
                <input class="input-field-name" type="text" id="name" required name="Nombre" autocomplete="off">
            
                <label class="label-input" for="mail">Mail*</label>
                <input class="input-field-mail" type="mail" id="mail" required name="Mail" autocomplete="off">
            
                <label class="label-input" for="number">Tu Whatsapp*</label>
                <input class="input-field-phone" type="text" id="number" required name="Whatsapp" autocomplete="off">

                <label class="label-input" for="instagram">Tu instagram</label>
                <input class="input-field-instagram" type="text" id="instagram" name="Instagram" autocomplete="off">
    
                <label class="label-input" for="massage">Cual es tu meta?</label>
                <textarea class="text-area-field" type="text" id="massage" name="Mensaje"
                >Hola! mi nombre es... y quiero empezar! </textarea>
                <div class="button-container">
                    <Button buttonValue="Enviar" img={Pesa_icono}></Button>
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


</style>