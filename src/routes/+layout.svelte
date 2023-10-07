<script>
  import "../app.postcss";
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavHamburger,
	} from "flowbite-svelte";
	import NavUl from "../NavUl.svelte";
</script>

<Navbar let:hidden let:toggle class="bg-gray-200 dark:bg-gray-900">
	<NavBrand href="/">
		<img
			src="https://raw.githubusercontent.com/donut2008/icse-sm.vercel.app/main/logo.svg"
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
		<NavLi href="/home" active={true}>Home</NavLi>
		<NavLi href="/banks">Question Banks</NavLi>
		<!-- question papers, decide whether to include answer keys or not -->
		<NavLi href="/programs">Programs</NavLi>
		<!-- programs in java, c++, and python -->
		<NavLi href="/about">About</NavLi>
	</NavUl>
</Navbar>

<slot />
