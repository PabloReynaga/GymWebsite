<script>
    import Button from './../../../componets/button.svelte'

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
                <input class="input-field" type="text" id="name" required name="Nombre">
            
                <label class="label-input" for="mail">Mail*</label>
                <input class="input-field" type="mail" id="mail" required name="Mail">
            
                <label class="label-input" for="number">Tu Whatsapp*</label>
                <input class="input-field" type="text" id="number" required name="Whatsapp">

                <label class="label-input" for="instagram">Tu instagram</label>
                <input class="input-field" type="text" id="instagram" name="Instagram" >
    
                <label class="label-input" for="massage">Cual es tu meta?</label>
                <textarea class="text-area-field" type="text" id="massage" name="Mensaje"
                >Hola! mi nombre es... y quiero empezar! </textarea>
                <div class="button-container">
                    <Button buttonValue="Enviar"></Button>
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

.input-field{
    justify-content: center;
    display:flex;
    text-align: left;
    box-sizing: border-box;
    padding: 8px;
    margin: auto;
    

}
.input-field:focus{
    outline: none;
    box-shadow:0px 0px 2px 2px $primary;
}
.input-field:hover{
    box-shadow:0px 0px 2px 2px $primary;
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
    width: 40vw;
    height: 15vh;
    padding: 8px;
    box-sizing: content-box;
    color: $bg-dark;
      
}
.text-area-field:hover{
    
    box-shadow:0px 0px 2px 2px $primary;
    
}
.text-area-field:focus{
    outline: none;
    box-shadow:0px 0px 2px 2px $primary;
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