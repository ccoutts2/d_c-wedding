<script lang="ts">
import '$lib/styles/globals.css'
import chris from '$lib/assets/Chris Picture.jpg';

import BurgerButton from "$lib/components/buttons/BurgerButton/BurgerButton.svelte";
import BurgerMenu from "$lib/components/BurgerMenu/BurgerMenu.svelte";
  import Message from '$lib/components/Message/Message.svelte';
  import Invitation from '$lib/components/Invitation/Invitation.svelte';
  import SectionHeader from '$lib/components/SectionHeader/SectionHeader.svelte';

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
<section id="home">
    <Invitation />
</section>

<section id="schedule">
    <SectionHeader label="Order of the day" />
</section>

<section id="travel">
    <SectionHeader label="Travel" />
</section>

<section id="qa">
    <SectionHeader label="Q & A" />
</section>

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
        flex-direction: column;
        justify-content: flex-start;
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

    section {
        margin: 100vh 0;
    }
</style>

