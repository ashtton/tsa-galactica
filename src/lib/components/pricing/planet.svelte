<script>
    import Tooltip from "sv-tooltip";
    import {chosenPlanet} from "$lib/stores/pricing_store.js";
    import {goto} from "$app/navigation";

    export let src;
    export let delay;
    export let miles;
    export let time;
    export let price;

    const formatter = new Intl.NumberFormat('en-US', {
        style: 'currency',
        currency: 'USD',
    });
</script>

<div class="planet {$chosenPlanet !== undefined && $chosenPlanet.name === src ? 'chosen' : ''}" on:click={() =>  chosenPlanet.set({
        name: src,
        miles: miles,
        time: time,
        price: parseFloat(price) / 900
})}>
    <Tooltip
            tip="<strong>{src.charAt(0).toUpperCase() + src.substring(1)}</strong><br>- {miles} Miles<br>- {time}<br>- {formatter.format(parseFloat(price) / 900)}"
            bottom>
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