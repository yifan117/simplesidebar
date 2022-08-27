<script lang="ts">
    import Magnify from "svelte-material-icons/Magnify.svelte";
    import Menu from "svelte-material-icons/Menu.svelte"
    import AccountCircle from "svelte-material-icons/AccountCircle.svelte";

    export let console: string;

    let links = ["🖕", "🤰"];

    function onClick(value: string) {
        console = console.concat(value);
    }

    function reset() {
        console = "";
    }
</script>

<div class="sidebar">
    <div class="icons">
        <div class="menu" on:click={() => reset()}>
            <Menu size="30px" />
        </div>
        <div class="div" />
        <div class="magnify">
            <Magnify size="30px" />
        </div>
    </div>
    <div class="links">
        {#each links as link}
            <div class="link" on:click={() => onClick(link)}>
                {link}
            </div>
        {/each}
    </div>
</div>

<style>
    .sidebar {
        display: flex;
        flex-direction: column;
        background-color: #595959;
        /* background-image: url("https://static.wikia.nocookie.net/despicableme/images/4/47/MTROG_Stuart.png/revision/latest/scale-to-width-down/350?cb=20220101205245"); */
        width: 50px;
        height: 100vh;
        padding: 8px;
        justify-content: space-between;
    }

    .icons {
        display: flex;
        flex-direction: column;
        gap: 8px;
        align-items: center;
    }

    .icons .menu {
        display: flex;
        padding: 6px;
        background-color: #595959;
    }

    .icons .menu:hover {
        background-color: #ffffff;
        opacity: 30%;
        border-radius: 4px;
        cursor: pointer;
    }

    .icons .magnify {
        display: flex;
        padding: 6px;
        border-radius: 4px;
    }

    .icons .magnify:hover {
        background-color: #ffffff;
        opacity: 30%;
        cursor: pointer;
    }

    .div {
        height: 2px;
        width: 42px;
        background-color: #ffffff;
    }

    .links {
        gap: 8px;
        display: flex;
        flex-direction: column;
        text-align: center;
        justify-content: center;
        align-items: center;
    }

    .links .link {
        font-size: 20px;
        gap: 8px;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        display: flex;
        padding: 6px;
        width: 30px;
        height: 30px;
        border-radius: 4px;
        text-align: center;
    }

    .links .link:hover {
        background-color: #ffffff;
        opacity: 30%;
        cursor: pointer;
        justify-content: center;
        text-align: center;
    }
</style>
