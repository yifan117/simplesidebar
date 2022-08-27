<script lang="ts">
import Sidebar from "../lib/components/Sidebar.svelte";

let abc = "";

</script>

<div class='body'>
    <Sidebar bind:console={abc}/>
    {abc}
</div>

<style>
* {
    margin: 0;
    padding: 0;
    border: 0;
}

.body {
    width: 100vh;
    height: 100vh;
    display: flex;
    margin: 0;
    padding: 0;
    border: 0;
    }





</style>