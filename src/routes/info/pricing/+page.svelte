<script>
    import {page} from "$lib/page_store.js";
    page.set("Pricing")

    import ChoosePlanet from '$lib/components/pricing/choose_planet.svelte'
    import ChooseRocket from '$lib/components/pricing/choose_package.svelte'
    import PriceCalc from '$lib/components/pricing/pricing_calculation.svelte'
    import {chosenPlanet, chosenPackage} from "$lib/stores/pricing_store.js";

</script>

<section class="animate__animated animate__fadeIn">
    <p class="title">Pricing Calculator</p>
    <p class="subtitle">Use this calculator to determine how much your trip will cost.</p>
    <ChoosePlanet />
    {#if $chosenPlanet !== undefined}
        <ChooseRocket />
    {/if}
    {#if $chosenPackage !== undefined}
        <PriceCalc />
    {/if}
</section>

<style>
    .title {
        margin-top: 2rem;
        font-weight: bold;
        font-size: 1.3rem;
    }

    .subtitle {
        margin-bottom: 1rem;
    }
</style>
