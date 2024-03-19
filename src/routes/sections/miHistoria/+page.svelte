<script>
    import img1 from '$lib/img/miHistoria_img1.png'
    import img2 from '$lib/img/miHistoria_img2.png'
    import img3 from '$lib/img/miHistoria_img3.png'
    import img4 from '$lib/img/miHistoria_img4.png'
    

</script>
<div class="main-container">
    <div class="title-container">
        <h1 class="title">Esta es mi historia...</h1>
    </div>
    <div class="text-container">
        <p class="text">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Eum ducimus id excepturi, vero, illum maxime modi dolor at voluptatibus molestias hic repellat, ipsum doloremque voluptate laudantium vel fugiat aliquid suscipit.
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ut illum totam quae dolorum quaerat commodi suscipit beatae officiis laboriosam pariatur. Similique debitis, possimus nemo velit dolore accusantium ex perferendis doloribus.
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maxime quos quam reiciendis nobis a perferendis, porro quidem sequi voluptatibus facere temporibus sed voluptates quia labore optio soluta, maiores minima placeat?
        </p>
    </div>
    <div class="images-container">
        <!-- <img class="img" alt="img" src={img1}> -->
        <img class="img first" alt="img" src={img2}>
        <img class="img" alt="img" src={img3}>
        <img class="img" alt="img" src={img4}>
    </div>
</div>
<style lang="scss">
    @import '../../../variables.scss';
    .main-container{
        width: 100%;
        height: auto;
        text-align: center;
        padding-top: 20px;

    }
    
    .title{
    font-size: 25px;
    text-align: center;
    text-transform: uppercase;
    color: $bg-bright;
    margin-bottom: 10px;
    }
    .text{
        font-size: 18px;
        text-align: center;
        color: $bg-bright;
        margin-bottom: 10px;
        font-weight: lighter;
      
    }
    .text-container{
        padding: 25px;
    }
    .images-container{
        display: flex;
        flex-wrap: wrap;
        height: 100%;
        min-width:100% ;
        
    }
    .img{
        height: 50%;
        width: 50%;

    }
    .first{
        width: 100%;
    }

</style>