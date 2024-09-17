<script lang="ts">
  import CountDown from "../CountDown/CountDown.svelte";


</script>

<section class="Invitation">

    <div class="Date Invitation__date">
        <p>Saturday</p>
        <p>July 11, 2026</p>
    </div>
    
    <p>Perthshire, TD3 6SD</p>

    <CountDown />

    
</section>

<style>

.Invitation {
    color: black;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.Invitation__date {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
</style>