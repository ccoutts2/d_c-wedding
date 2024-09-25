<script lang="ts">
  import CountDown from "../CountDown/CountDown.svelte";

</script>

<div class="Invitation" id="schedule">

    <dl class="Date Invitation__date">
        <dt class="visually-hidden">Date:</dt>
        <dd><time datetime="2026-07-11">Saturday, July 11, 2026</time></dd>
        <dt class="visually-hidden">Location:</dt>
        <dd>Dunkeld, Perthshire, TD3 6SD</dd>
        <dt class="visually-hidden">Wedding is in:</dt>
        <dd><CountDown /></dd>
    </dl>
    
</div>

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