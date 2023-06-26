<script>
	// The ordering of these imports is critical to your app working properly
	import "@skeletonlabs/skeleton/themes/theme-gold-nouveau.css"
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import "@skeletonlabs/skeleton/styles/skeleton.css"
	// Most of your app wide CSS should be put in this file
	import "../app.postcss"

	import { AppShell } from "@skeletonlabs/skeleton"
	import Sidebar from "../lib/Sidebar.svelte";
</script>


<AppShell>
	<svelte:fragment slot="header">Header</svelte:fragment>
	<svelte:fragment slot="sidebarLeft">
		<Sidebar />
	</svelte:fragment>
	<!-- (sidebarRight) -->
	<!-- (pageHeader) -->
	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->
	<svelte:fragment slot="pageFooter">Page Footer</svelte:fragment>
	<!-- (footer) -->
</AppShell>