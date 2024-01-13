<script>

export let text;
export let height;
export let width;
export let title;
export let iconSorce;
export let iconSize;



</script>
<div class="main-container" style="height: {height}; width: {width};">
    <div class="icon-container">
        <img alt="img" class="main-icon" style="width: {iconSize};" src={iconSorce}>
    </div>
    
    <div class="title-container">
        <p class="title">{title}</p>
        <p class=text>{text}</p>
    </div>
    
</div>


<style lang="scss">
.main-container{
    display: flexbox;
    justify-content: center;
    
   text-align: center;
   padding: 25px;
   border: 3px solid $primary;
   border-radius: 5px;
   margin: 25px;
    
}
.text{
    font-size: 15px;
    text-align: center;
    
}
.title{
    font-size: 18px;
    text-align: center;
    
    margin-bottom: 10px;
}
.icon-container{
    display: flex;
    margin: auto;
    justify-content: center;
    background-color: rgba($color: #ffc6c6, $alpha: .3);
    width: 65px;
    border-radius: 100px;
}
.main-icon{
    margin: 5px;
    
}

</style>

