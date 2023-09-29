<script>
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
	} from "flowbite-svelte";
</script>

<Navbar let:hidden let:toggle>
	<NavBrand href="/">
		<img
			src="https://flowbite.com/docs/images/logo.svg"
			class="mr-3 h-6 sm:h-9"
			alt="Flowbite Logo"
		/>
		<span
			class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
		>
			NoteMaster
		</span>
	</NavBrand>
	<NavHamburger on:click={toggle} />
	<NavUl {hidden}>
		<NavLi href="/" active={true}>Home</NavLi>
		<NavLi href="/">Question banks</NavLi> <!-- question papers, decide whether to include answer keys or not -->
		<NavLi href="/">Programs</NavLi> <!-- programs in java, c++, and python -->
		<NavLi href="/about">About</NavLi>
	</NavUl>
	<!-- I'LL WORK ON THIS AFTER I RETURN FROM KOLKATA -->
</Navbar>