<script>
    import {page} from "$lib/page_store.js";
    page.set("Pricing")

    import ChoosePlanet from '$lib/components/pricing/choose_planet.svelte'
</script>

<section class="animate__animated animate__fadeIn">
    <h1>Pricing Calculator</h1>
    <ChoosePlanet />
</section>
