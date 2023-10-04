<script>
    import { page } from "$app/stores";
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
        P,
	} from "flowbite-svelte";
    $: activeUrl = $page.url.pathname;
    let activeClass =
        "text-white bg-green-700 md:bg-transparent md:text-green-700 md:dark:text-white dark:bg-green-600 md:dark:bg-transparent";
    let nonActiveClass =
        "text-gray-700 hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-green-700 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent";
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
	<NavUl {activeUrl} {activeClass} {nonActiveClass}>
		<NavLi href="/home">Home</NavLi>
		<NavLi href="/banks">Question banks</NavLi> <!-- question papers, decide whether to include answer keys or not -->
		<NavLi href="/programs" active={true}>Programs</NavLi> <!-- programs in java, c++, and python -->
		<NavLi href="/about">About</NavLi>
	</NavUl>
</Navbar>
<div class="text-center">
    <P class="mb-6 text-lg lg:text-xl sm:px-16 xl:px-48 dark:text-gray-400">there should be programs here smh</P>
</div>