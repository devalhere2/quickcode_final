<script>
    import { goto } from "$app/navigation";
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
<nav>
    <h1 on:click={() => goto("/")}>Quickcode</h1>
    <div>
        <button on:click={() => goto("/login")}>Login</button>
    </div>
</nav>

<style lang="scss">
    nav {
        padding: 0 10vw;
        border-bottom: 1px solid gray;
        display: flex;
        align-items: center;
        h1 {
            flex: 1;
        }
    }
</style>
