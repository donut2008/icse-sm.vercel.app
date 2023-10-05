<script>
	import { Navbar, NavBrand, NavLi, NavHamburger, Heading, P } from "flowbite-svelte";
	import NavUl from "../../NavUl.svelte";
</script>

<Navbar let:hidden let:toggle>
	<NavBrand href="/">
		<img
			src="https://flowbite.com/docs/images/logo.svg"
			class="mr-3 h-6 sm:h-9"
			alt="ICSE Study Material Logo"
		/>
		<span
			class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
		>
			ICSE Study Material
		</span>
	</NavBrand>
	<NavHamburger on:click={toggle} />
	<NavUl>
		<NavLi href="/home">Home</NavLi>
		<NavLi href="/banks">Question banks</NavLi>
		<NavLi href="/programs">Programs</NavLi>
		<NavLi href="/about" active={true}>About</NavLi>
	</NavUl>
</Navbar>
<div class="text-left sm:px-16 xl:px-48">
	<Heading tag="h2" customSize="pt-6 text-2xl font-medium md:text-xl lg:text-4xl text-black dark:text-white">About</Heading>
	<P class="mb-6 text-lg lg:text-xl pt-6 dark:text-gray-400"
		>This website is a hobby project made possible by me, donut, and a few
		other friends who helped me to gather the content for this website.</P
	>
</div>
