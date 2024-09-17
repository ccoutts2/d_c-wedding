<script lang="ts">
 export let toggleMenu: () => void;
 export let isOpen: boolean;
</script>

<button type="button" on:click={toggleMenu} class:open={isOpen}>
    {isOpen ? "Close" : "Menu"}
</button>

<style>
    button {
        left: 1rem;
        position: fixed;
        top: 1rem;
        z-index: 10;
        padding: 0.4rem 2rem;
        min-width: 7rem;
        background: rgba(255, 255, 255, 0.72);
        backdrop-filter: saturate(180%) blur(20px);
        border-radius: 1rem;
        color: black;
        box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.1),0px 10px 15px -3px rgba(0,0,0,0.1);
    }
</style>