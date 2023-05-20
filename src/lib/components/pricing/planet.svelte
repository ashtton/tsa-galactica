<script>
    import Tooltip from "sv-tooltip";
    import {chosenPlanet} from "$lib/stores/pricing_store.js";

    export let src;
    export let delay;
    export let miles;
    export let time;
</script>

<div class="planet {$chosenPlanet !== undefined && $chosenPlanet.name === src ? 'chosen' : ''}" on:click={() => chosenPlanet.set({
    name: src,
    miles: miles,
    time: time,
})}>
    <Tooltip tip="<strong>{src.charAt(0).toUpperCase() + src.substring(1)}</strong><br>- {miles} Miles<br>- {time}" bottom>
        <img alt="{src}" style="--animate-delay: {delay}"
             class="image animate__animated animate__fadeIn animate__delay-1s" height="72px"
             src="/images/planets/{src}.png">
    </Tooltip>
</div>

<style>
    .planet {
        cursor: pointer;
    }

    .image:hover, .chosen .image {
        scale: 125%;
        transition: all .2s ease-in-out;
        filter: grayscale(100%);
    }
</style>