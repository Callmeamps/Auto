<script>
    import { AppBar } from "@skeletonlabs/skeleton";

    const pages = ["Home", "Dashboard", "Projects", "Posts", "Chats", "Agents", "Notes"]
    
    const icons = ["https://fav.farm/🙏🏿", "https://fav.farm/🖥"]
</script>
<AppBar>
    <svelte:fragment slot="lead">
        <a href="/" class="m-3">
            <img src="{icons[0]}" alt="Home Icon; Fire" class="w-5 h-5"> 
        </a>
    </svelte:fragment>
    {#each pages as page}
        <a href="/{`${page === "Home" ? "" : page.toLocaleLowerCase()}`}" class="btn m-1 variant-ghost">{page}</a>
    {/each}
    <svelte:fragment slot="trail">
        <a href="/login" class="btn-icon m-3 variant-ghost">
            <img src="{icons[1]}" alt="Login Icon; Computer" class="w-5 h-5"> 
        </a>
    </svelte:fragment>
</AppBar>