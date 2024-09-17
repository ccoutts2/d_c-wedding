<script lang="ts">
import '$lib/styles/globals.css'
import chris from '$lib/assets/Chris Picture.jpg';

import BurgerButton from "$lib/components/buttons/BurgerButton/BurgerButton.svelte";
import BurgerMenu from "$lib/components/BurgerMenu/BurgerMenu.svelte";

export let isOpen: boolean = false;
const toggleMenu = () => {
        isOpen =!isOpen;
    }  
</script>

<main>
<nav>
    <BurgerButton {toggleMenu} {isOpen} />
</nav>

<BurgerMenu {isOpen} />

<div class='Image'>
    <img src={chris} alt=""/>
</div>


<slot />
</main>

<style>
    main {
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        height: 300vh;
    }

    .Image {
        height: 100vh;
        position: fixed;
        width: 50%;
    }

    .Image img {
        height: 100%;
        object-fit: cover;
        width: 100%;
    }
</style>

