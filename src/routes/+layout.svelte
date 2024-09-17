<script lang="ts">
import '$lib/styles/globals.css'
import chris from '$lib/assets/Chris Picture.jpg';

import BurgerButton from "$lib/components/buttons/BurgerButton/BurgerButton.svelte";
import BurgerMenu from "$lib/components/BurgerMenu/BurgerMenu.svelte";
  import Message from '$lib/components/Message/Message.svelte';
  import Invitation from '$lib/components/Invitation/Invitation.svelte';

export let isOpen: boolean = false;
const toggleMenu = () => {
        isOpen =!isOpen;
    }  
</script>

<main>
<div class="LeftCol">
<nav>
    <BurgerButton {toggleMenu} {isOpen} />
</nav>

<BurgerMenu {isOpen} />

<div class='Image'>
    <img src={chris} alt=""/>
</div>

<Message />
</div>

<div class="RightCol">
<Invitation />
</div>


<slot />
</main>

<style>
    main {
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        height: 300vh;
        display: flex;
        justify-content: center;
    }

    .LeftCol {
        flex: 1.2 ;
    }
    
    .RightCol {
        flex: 1;
        display: flex;
        justify-content: center;
    }

    .Image {
        height: 100vh;
        position: fixed;
        width: 55%;
    }

    .Image img {
        height: 100%;
        object-fit: cover;
        width: 100%;
    }
</style>

