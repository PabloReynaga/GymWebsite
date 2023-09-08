<script>
	import './../../src/index.css'
   $: windowsWidth-=50;
   $: margin_left = windowsWidth -65;


  let isDropdownOpen = false 

  const handleDropdownClick = () => {
    isDropdownOpen = !isDropdownOpen
  }

  const handleDropdownFocusLoss = ({ relatedTarget, currentTarget }) => {
   
    if (relatedTarget instanceof HTMLElement && currentTarget.contains(relatedTarget)) return 
    isDropdownOpen = false
  }
</script>
<svelte:window bind:innerWidth={windowsWidth}/>

<div class="prueba">
	<div class="dropdown-menu" on:focusout={handleDropdownFocusLoss}>
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
		
		<ul style="width:{windowsWidth}px; margin-left: -{margin_left}px;}" class="dropdown-content menu p-2 shadow bg-base-200 rounded-box " style:display={isDropdownOpen ? 'flex' : 'none'}>
			<li><button class="item btn m-2 w-45" on:click={handleDropdownClick}><a href="https://5d09-84-46-89-26.ngrok-free.app/#home">Inicio</a></button></li>
			<li><button class="item btn m-2 w-45 " on:click={handleDropdownClick}><a  href="https://5d09-84-46-89-26.ngrok-free.app/#about">Transformación</a></button></li>
            <li><button class="item btn m-2 w-45" on:click={handleDropdownClick}><a  href="https://5d09-84-46-89-26.ngrok-free.app/#vlog">Mi Misión</a></button></li>
            <li><button class="item btn m-2 w-45" on:click={handleDropdownClick}><a  href="https://5d09-84-46-89-26.ngrok-free.app/#contact">Contactame</a></button></li>
        
		</ul>
	</div>
	
	
</div>
<style lang="scss">


.dropdown-content{
	justify-content: center;
	display: flex;
	
	height: 400px;
	width: 600px;
	background-color: #3a3a3b;
	z-index: 999999;
	
	
	
}
.item{
	height: 70px;
	font-size: 17px;
	
    display:flex;
	align-items: center;
	vertical-align: middle;
	text-align: center;
	a{
		display:flex;
		align-items: center;
		vertical-align: middle;
		margin-top: 18px;
		
	}
	
}

.prueba{
	position:absolute;
	margin-top: -25px;
	margin-left: -40px;
	

}



.prueba{
	position:absolute;
	margin-top: -25px;
	margin-left: -40px;
	
}
   
</style>