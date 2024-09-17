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
        padding: 0.25rem 0.75rem;
        background: rgba(255, 255, 255, 0.72);
        backdrop-filter: saturate(180%) blur(20px);
    }

    button::before {
        content: "";
    }


    button.open::before {
        content: "please ";
    }
</style>