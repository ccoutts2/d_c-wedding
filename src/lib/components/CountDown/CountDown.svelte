<script lang="ts">

import { onMount } from "svelte";

interface remainingTimeProps {
    days: number,
    hours: number,
    minutes: number,
};

let weddingDate: any = new Date("2026-07-11T00:00:00");
let remainingTime: remainingTimeProps = {
    days: 0,
    hours: 0,
    minutes: 0,
}
let interval: number;



const countdownToWedding = () => {

    let now: any = new Date();
    let difference: any = weddingDate - now;

    if (difference > 0){
        remainingTime = {
            days: Math.floor(difference / (1000 * 60 * 60 * 24)),
            hours: Math.floor(difference % (1000 * 60 * 60 * 24) / (1000 * 60 * 60)),
            minutes: Math.floor(difference % (1000 * 60 * 60) / (1000 * 60)),
        }
    } else {
        clearInterval(interval);
        remainingTime = {
            days: 0,
            hours: 0,
            minutes: 0,
        }
    }
}

onMount(() => {
    countdownToWedding();
    interval = setInterval(countdownToWedding, 1000);

    return () => {
        clearInterval(interval);
    }
})
</script>

<div class="Countdown">
    <span>{remainingTime.days}</span> <span>days</span>
    <span>{remainingTime.hours}</span> <span>hrs</span>
    <span>{remainingTime.minutes}</span> <span>mins</span>
</div>

<style>
   .Countdown {
    text-transform: uppercase;
   }
</style>