<script context="module">
	export const prerender = true;
</script>

<script>
  import {
    Menu,
    MenuButton,
    MenuItems,
    MenuItem,
 
  } from "@rgossiaux/svelte-headlessui";
 import { fade } from "svelte/transition";
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="container-lg h-[100vh]">
	<h1 class="text-7xl font-black text-center">
	velte<br> Headless ui
	</h1>
<Menu let:open>
  <MenuButton class="z-0 bg-blue-700 px-5  py-1 rounded text-white text-xl font-semibold shadow-lg shadow-blue-700 ">More</MenuButton>
	 {#if open}
	  <div transition:fade>
	 
  <MenuItems class="z-50 p-5 mt-2 bg-slate-100 flex flex-col w-[200px] rouned-lg shadow-xl">
    <MenuItem let:active>
      <a class="hover:bg-blue-700 w-[200px] hover:text-white/90" href="/">Account settings</a>
    </MenuItem>
    <MenuItem let:active>
      <a href="/" class:active>Documentation</a>
    </MenuItem>
    <MenuItem disabled>
      <span class="disabled">Invite a friend (coming soon!)</span>
    </MenuItem>
  </MenuItems>
	</div>
	{/if}
</Menu>


 
</section>

<style>
	section {

	}

</style>
