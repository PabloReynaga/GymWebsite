<svelte:head>	
<link href="https://cdn.jsdelivr.net/npm/daisyui@2.11.0/dist/full.css" rel="stylesheet" type="text/css" />
<script src="https://cdn.tailwindcss.com"></script>
</svelte:head>


// add text here if REPL preview is empty 


<script>
   $: windowsWidth-=50;
   $:console.log(windowsWidth+"!");
   $: margin_left = windowsWidth -90;


  let isDropdownOpen = false // default state (dropdown close)

  const handleDropdownClick = () => {
    isDropdownOpen = !isDropdownOpen // togle state on click
  }

  const handleDropdownFocusLoss = ({ relatedTarget, currentTarget }) => {
    // use "focusout" event to ensure that we can close the dropdown when clicking outside or when we leave the dropdown with the "Tab" button
    if (relatedTarget instanceof HTMLElement && currentTarget.contains(relatedTarget)) return // check if the new focus target doesn't present in the dropdown tree (exclude ul\li padding area because relatedTarget, in this case, will be null) 
    isDropdownOpen = false
  }
</script>
<svelte:window bind:innerWidth={windowsWidth}/>

<div class="prueba">
	<div class="dropdown" on:focusout={handleDropdownFocusLoss}>
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
		<ul style="width:{windowsWidth}px; margin-left: -{margin_left}px;}" class="dropdown-content menu p-2 shadow bg-base-200 rounded-box " style:visibility={isDropdownOpen ? 'visible' : 'hidden'}>
			<li><button class="item btn text-slate-400 m-2 w-45"><a href="#home">Inicio</a></button></li>
			<li><button class="item btn text-slate-300  m-2 w-45 "><a href="#about">Trasformación</a></button></li>
            <li><button class="item btn text-slate-300 m-2 w-45"><a href="#vlog">Mi Misión</a></button></li>
            <li><button class="item btn text-slate-300 m-2 w-45"><a href="#contact">Contactame</a></button></li>
        
		</ul>
	</div>
	
</div>
<style>
.prueba{
   display: flex;
   justify-content: right;
   

}
.button{
    
    width: auto;
    margin-right: 8px;
}
.dropdown-content{
	
	
	padding: 15px;
	
	height: 400px;
	justify-content: center;
	display: flex;
}
.item{
	height: 70px;
	font-size: 17px;
	
}



    
</style>