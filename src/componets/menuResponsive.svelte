<script>
import icon from '$lib/icon/main-icon.png'
import iconInstagram from '$lib/icon/instagram-black.png'
import iconMail from '$lib/icon/mail-black.png'
import gsap from 'gsap';

let animationMenu;
let animationLostFocus;
let item1;
let item2;
let item3;
let item4;
let icon1;
let icon2
let isMenuOpen = false 


const handleDropdownClick = () => {
	
	if(isMenuOpen==true){
		let tl = gsap.timeline( {onComplete: changeIsMenuOpenValue });
		tl.fromTo(animationMenu,{x:0},{x:500, duration:.8})
   		   .fromTo(animationLostFocus,{x:0},{x:-500, duration:.8,},"<")
		   
	}else{
		isMenuOpen = !isMenuOpen

		gsap.fromTo(animationMenu,{x:500},{x:0, duration:.7})
		gsap.fromTo(animationLostFocus,{x:-500},{x:0, duration:.5})
	
		gsap.fromTo(item1,{x:1000},{x:0,duration:.1})
		gsap.fromTo(item2,{x:1000},{x:0,duration:.2})
		gsap.fromTo(item3,{x:1000},{x:0,duration:.3})
		gsap.fromTo(item4,{x:1000},{x:0,duration:.4})
		gsap.fromTo(icon1,{y:600},{y:0,duration:.9})
		gsap.fromTo(icon2,{y:600},{y:0,duration:1.2})
	}
}

function handleDropdownFocusLoss() {

	let tl = gsap.timeline( {onComplete: changeIsMenuOpenValue });
		tl.fromTo(animationMenu,{x:0},{x:500, duration:.8})
   		.fromTo(animationLostFocus,{x:0},{x:-500, duration:.8,},"<")
		
}
function changeIsMenuOpenValue(){
	isMenuOpen = false
}
</script>

<button class="button btn " on:click={()=>{handleDropdownClick()}} >
	{#key isMenuOpen}
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
									stroke-width="3"
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
									stroke-width="3"
									d="M4 6h16M4 12h16M4 18h16" />
							</svg>
			{/if}
		
	{/key}
		
</button>
<div bind:this={animationMenu} class={isMenuOpen? "menu-container-open":"menu-container-close"} >
		<div class="sidebar-menu" >
			<img src={icon} alt="img" class="icon">
			<nav class="nav-items">
			<a href="#home" class="item" on:click={handleDropdownClick} bind:this={item1}>Inicio</a>
			<div class="details-lines" style="width: 45px;"></div>
			<a  href="#about" class="item" on:click={handleDropdownClick} bind:this={item2}>Transformación</a>
			<div class="details-lines" style="width: 120px;"></div>
			<a  href="#vlog" class="item" on:click={handleDropdownClick} bind:this={item3}>Mi Misión</a>
			<div class="details-lines" style="width: 75px;"></div>
			<a  href="#contact" class="item" on:click={handleDropdownClick} bind:this={item4}>Contactame</a>
			<div class="details-lines" style="width: 95px;"></div>
			</nav>
			<div class="footer-menu">
				<div class="container-icons-instagram" bind:this={icon1} >
					<a href="https://instagram.com/cacholofitness?igshid=MzRlODBiNWFlZA==">
							<img class="icon-instagram" alt="img" src={iconInstagram}>
					</a>
		
				</div>
				<div class="container-icons-mail" bind:this={icon2}>
					<a href="https://www.youtube.com/@CacholoFitness">
							<img class="icon-mail" alt="img" src={iconMail}>
					</a>
					
		
				</div>
			</div>
		</div>
		
</div>
<button class={isMenuOpen?"focus-lost":"focus-lost-close"} on:click={handleDropdownFocusLoss} bind:this={animationLostFocus}></button>

<style lang="scss">
@import '../variables.scss';

.sidebar-menu{
	position: relative;
	height: 100%;
	width: 100%;
	background-color: $bg-dark;
	
}

.menu-container-close{
	position:absolute;
	height: 100%;
	width: 0%;
	right: -500px;
	
}
.menu-container-open{
	position:absolute;
	height: 1200px;
	width: 80%;
	right: 0px;
	z-index: 0;
	margin-top: -70px;
	z-index: 100;
}


.focus-lost{
	position: absolute;
	top:0;
	left: 0;
    min-height: 1200px;
	width: 60%;
	background-color: $bg-dark-gray;
	opacity: .5;
	z-index: 10;
	
	
}
.focus-lost-close{
	position: absolute;
	left: 0;
	width: 0%;
	
	
}

.item{
	display: flex;
	font-size: 18px;
	justify-content: left;
	margin-left: 30px;
	color: $bg-bright;
	margin-top: -10px;
	align-items: center;
	height: 70px;
	
	

}
.icon{
	transform: scale(.3);
	margin: auto;
	 margin-top: -15px;
	
}
.button{
	position: relative;
	z-index: 200;
}
.nav-items{
	margin-top: -80px;
}
.details-lines{
	display: flex;
	border: solid 1px $primary;
	margin: auto;
	margin-top: -20px;
	margin-bottom: 30px;
	margin-left: 30px;
	width: 10%;
	

}

.icon-instagram{
	height: 30px;
	margin: auto
}
.icon-mail{
	height: 30px;
	margin: auto
}
.footer-menu{
	display: flex;
	justify-content: right;
	margin-top: 70px;
	
}
.container-icons-mail{
	background-color: $primary;
	border-radius: 25px;
	padding: 10px;
	margin: auto;
	margin-left: 10px;
	width: 30%;
	
}
.container-icons-instagram{
	background-color: $primary;
	border-radius: 25px;
	padding: 10px;
	margin: auto;
	margin-right: 10px;
	width: 30%;
	

	
}
   
</style>