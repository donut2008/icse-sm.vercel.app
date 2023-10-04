<script>
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
        Heading,
        P,
	} from "flowbite-svelte";
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
	<NavUl {hidden}>
		<NavLi href="/home" active={true}>Home</NavLi>
		<NavLi href="/banks">Question banks</NavLi> <!-- question papers, decide whether to include answer keys or not -->
		<NavLi href="/programs">Programs</NavLi> <!-- programs in java, c++, and python -->
		<NavLi href="/about">About</NavLi>
	</NavUl>
</Navbar>
<div class="text-center">
    <P class="mb-6 text-lg lg:text-xl sm:px-16 xl:px-48 dark:text-gray-400">where questions</P>
</div>