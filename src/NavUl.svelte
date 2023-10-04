<script>
    import { page } from "$app/stores";
    import { NavUl } from "flowbite-svelte";
    $: activeUrl = $page.url.pathname;
    let activeClass =
        "text-white bg-green-700 md:bg-transparent md:text-green-700 md:dark:text-white dark:bg-green-600 md:dark:bg-transparent";
    let nonActiveClass =
        "text-gray-700 hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-green-700 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent";
</script>

<NavUl {activeUrl} {activeClass} {nonActiveClass}>
    <slot />
</NavUl>
