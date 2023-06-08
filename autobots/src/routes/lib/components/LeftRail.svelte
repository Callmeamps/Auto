<script>
    import { AppRail, AppRailTile } from "@skeletonlabs/skeleton";
    let currentTile = 0;
</script>

<AppRail>
	
    <AppRailTile bind:group={currentTile} name="tile-1" value={0} title="tile-1">
        <svelte:fragment slot="lead">(icon)</svelte:fragment>
        <span>Tile 1</span>
    </AppRailTile>
					
</AppRail>