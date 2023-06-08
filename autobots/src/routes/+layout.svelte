<script>
	import { AppShell } from '@skeletonlabs/skeleton';
	import Nav from './lib/components/Nav.svelte';
	import LeftRail from './lib/components/LeftRail.svelte';
	// The ordering of these imports is critical to your app working properly
	import '../theme.postcss';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
</script>
<AppShell>
	<svelte:fragment slot="header">
		<!-- <Navbar/> -->
		<Nav/>
	</svelte:fragment>
	<svelte:fragment slot="sidebarLeft">
		<!-- <Sidebar/> -->
		<LeftRail />
	</svelte:fragment>
	<!-- (sidebarRight) -->
	<!-- (pageHeader) -->
	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->
	<svelte:fragment slot="pageFooter">Page Footer</svelte:fragment>
	<!-- (footer) -->
</AppShell>
