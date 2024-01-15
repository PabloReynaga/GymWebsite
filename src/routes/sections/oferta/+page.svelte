<script>
    import Button from './../../../componets/button.svelte'

</script>
<div class="main-container">
    <div class="title-container">
        <h1 class="title">Inicia tu cambio <span style="color: #e21135;">Hoy</span></h1>
    </div>
    
    <div class="card-container">
        <div class="mejor-oferta-container"><p style="font-size: 18px;">Mejor oferta</p></div>
      <p class="subtitle">PLAN DE NUTRICIÓN Y ENTRENAMIENTO <span style="color:#e21135 ;">PERSONALIZADO</span></p> 
        <p class="price">260€<span style="font-size: 12px; margin-left: 10px;">trimestral</span></p>
        <Button text={"Inicia ahora"} width={"200px"}></Button>
        <p style="font-size: 12px; margin-top: 5px">*Suscripción trimestral recurrente*</p>
    </div>
    <div class="info-container">
        <p class="item">✔ Plan de nutrición y entrenamiento personalizado según tus objetivos</p>
        <p class="item">✔ Variedad de opciones de alimentación de acuerdo a tus gustos</p>
        <p class="item">✔ Rastreador de progreso</p>
        <p class="item">✔ Demostración de ejercicios en video</p>
        <p class="item">✔ Lista de compras</p>
        <p class="item">✔ Videollamadas</p>
        <p class="item">✔ Aplicación móvil exclusiva</p>
        <p class="item">✔ Soporte por correo electrónico 24h</p>
        <p class="item">✔ Soporte por whatsapp 24h</p>
        <p class="item">✔ Acceso Comunidad del TEAM TRILLO</p>
    </div>
</div>
<style lang="scss">
    @import '../../../variables.scss';
    .main-container{
        width: 100%;
        height: auto;
        text-align: center;
        padding: 20px;

    }
    .title-container{
       max-width: 200px;
       display: flex;
       margin: auto;
    }
    .title{
    font-size: 28px;
    text-align: center;
    text-transform: uppercase;
    color: $bg-bright;
    margin-bottom: 25px;
  
    }
    .text-container{
        padding: 25px;
    }
    .card-container{
        display: block;
        width: 90%;
        height: auto;
        margin: auto;
        background-color:#333 ;
        border-radius: 15px;
        padding: 35px;
    }
    .subtitle{
        font-size: 20px;
        padding-left: 20px;
        padding-right:20px;
        padding-top: 20px;
        
    }
    .price{
        font-size: 60px;
        
    }
    .info-container{
        width: 80%;
        height: auto;
        margin: auto;
        margin-top: 30px;
        background-color: #333;
        border-radius: 15px;
        padding: 25px;
    }
    .item{
        font-size: 18px;
    }
    .mejor-oferta-container{
        position: relative;
        background-color: $primary;
        padding: 15px;
        padding-top: 8px;
        padding-bottom: 8px;
        margin: auto;
        margin-top: -53px;
        width: 200px;
        
        
        
    }
</style>