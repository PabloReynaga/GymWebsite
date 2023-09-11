<script>
	import './../../src/index.css'
   $: windowsWidth-=50;
   $: margin_left = windowsWidth -65;


  let isDropdownOpen = false 
  

  const handleDropdownClick = () => {
    isDropdownOpen = !isDropdownOpen
  }

  const handleDropdownFocusLoss = () => {
   
    if(isDropdownOpen === true){
		isDropdownOpen=false
	}
  }
</script>
<svelte:window bind:innerWidth={windowsWidth}/>

<div class="main-container">
	<div class="dropdown-menu" >
		<button class="button btn " on:click={handleDropdownClick} >
		{#if isDropdownOpen}
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
		<nav >
			<div style="width:{windowsWidth}px; margin-left: -{margin_left}px;}" class="dropdown-content menu p-2 shadow bg-base-200 rounded-box " style:display={isDropdownOpen ? 'flex' : 'none'}>
				
				<a href="#home" class="item btn m-2 w-45" on:click={handleDropdownClick}>Inicio</a>
				<a  href="#about" class="item btn m-2 w-45" on:click={handleDropdownClick}>Transformación</a>
				<a  href="#vlog" class="item btn m-2 w-45" on:click={handleDropdownClick}>Mi Misión</a>
				<a  href="#contact" class="item btn m-2 w-45" on:click={handleDropdownClick}>Contactame</a>

			</div>
			<button class="focus-lost" on:click={handleDropdownFocusLoss} style:display={isDropdownOpen ? 'flex' : 'none'}></button>

		</nav>
		
	</div>
	
	
</div>
<style lang="scss">


.dropdown-content{
	justify-content: center;
	display: flex;
	height: 400px;
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

.main-container{
	position:absolute;
	margin-top: -25px;
	margin-left: -40px;
}


.focus-lost{
    background-color: transparent;
    height: 50%;
    width: 150%;
	float: right;
	margin-left: -100%;
    position: fixed;


}
   
</style>