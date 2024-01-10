<script>
import './../../src/index.css'
import icon from '$lib/icon/main-icon.png'

let isMenuOpen = false 
  

  const handleDropdownClick = () => {
    isMenuOpen = !isMenuOpen
  }

  const handleDropdownFocusLoss = () => {
   
    if(isMenuOpen === true){
		isMenuOpen=false
	}
  }
</script>

<button class="button btn " on:click={handleDropdownClick} >
		{#if isMenuOpen}
			<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								class="inline-block h-6 w-6 stroke-current">
								<title>Close Dropdown</title>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M6 18L18 6M6 6l12 12" />
							</svg>
			{:else}
			<svg
								xmlns="http://www.w3.org/2000/svg"
								fill="none"
								viewBox="0 0 24 24"
								class="inline-block h-6 w-6 stroke-current">
								<title>Open Dropdown</title>
								<path
									stroke-linecap="round"
									stroke-linejoin="round"
									stroke-width="2"
									d="M4 6h16M4 12h16M4 18h16" />
							</svg>
			{/if}
</button>
<div class={isMenuOpen? "menu-container-open":"menu-container-close"}>
		<div class="sidebar-menu">
			<img src={icon} alt="img" class="icon">
			<nav class="nav-items">
			<a href="#home" class="item" on:click={handleDropdownClick}>Inicio</a>
			<div class="details-lines"></div>
			<a  href="#about" class="item" on:click={handleDropdownClick}>Transformación</a>
			<div class="details-lines"></div>
			<a  href="#vlog" class="item" on:click={handleDropdownClick}>Mi Misión</a>
			<div class="details-lines"></div>
			<a  href="#contact" class="item" on:click={handleDropdownClick}>Contactame</a>
			<div class="details-lines"></div>

			</nav>
			

		</div>
</div>
<button class={isMenuOpen?"focus-lost":"focus-lost-close"} on:click={handleDropdownFocusLoss} ></button>
<style lang="scss">


.dropdown-content{
	justify-content: center;
	display: flex;
	height: 100%;
	width: 600px;
	background-color: #3a3a3b;	
}
.item{
	height: 70px;
	font-size: 17px;
    display:flex;
	align-items: center;
	vertical-align: middle;
	text-align: center;
}

.menu-container-close{
	position:absolute;
	height: 900px;
	width: 0%;
	right: -500px;
	
}
.menu-container-open{
	position:absolute;
	min-height: 100%;
	width: 80%;
	right: 0px;
	z-index: 0;
	margin-top: -70px;
}


.focus-lost{
	position: absolute;
	left: 0;
	top: 0;
    min-height: 900px;
    width: 100px;
	max-width: 20%;
	background-color: $bg-dark;
	opacity: .5;
	
}
.focus-lost-close{

}
.sidebar-menu{
	display: block;
	height: 900px;
	width: 100%;
	background-color: $bg-dark;
	
}
.item{
	font-size: 18px;
	justify-content: left;
	margin-left: 30px;
	color: $bg-bright;
	margin-top: -10px;
	

}
.icon{
	transform: scale(.4);
	margin: auto;
	 
	
}
.button{
	position: relative;
	z-index: 100;
	
	
}
.nav-items{
	margin-top: -80px;
}
.details-lines{
	border: solid 1px $primary;
	margin-top: -10px;
	margin-bottom: 30px;

}
   
</style>