<script>
    import {chosenPlanet, chosenPackage} from "$lib/stores/pricing_store.js";


    const formatter = new Intl.NumberFormat('en-US', {
        style: 'currency',
        currency: 'USD',
    });

    let currentPrice

    $: {
        console.log($chosenPlanet)
        currentPrice = $chosenPlanet.price + $chosenPackage.price + 50
    }

</script>

<div id="price" class="step animate__animated animate__fadeInDown">
    <div class="price-steps">
        <div>Visiting <strong>{$chosenPlanet.name.charAt(0).toUpperCase() + $chosenPlanet.name.substring(1)}</strong></div>
        <div>Fuel Cost<span class="price">{formatter.format($chosenPlanet.price)}</span></div>
        {#if $chosenPackage.name !== "standard"}
            <div>{$chosenPackage.name.charAt(0).toUpperCase() + $chosenPackage.name.substring(1)} Package<span class="price">{formatter.format($chosenPackage.price)}</span></div>
        {/if}
        <div>Training Course<span class="price">$500.00</span></div>
        <div>Tax<span class="price">{formatter.format(currentPrice * 0.1)}</span></div>
        <hr>
        <div>Total Cost: <span class="price">{formatter.format(currentPrice * 1.1)}</span></div>
    </div>
</div>

<style>
    .price {
        font-weight: bold;
        font-size: 2rem;
    }

    .price-steps {
        margin-top: 3rem;
        font-size: 1.5rem;
    }

    .price-steps div:not(:first-child) {
        margin-left: 1rem;
        display: flex;
        justify-content: space-between;
    }

    @media(max-width: 450px) {
        .price-steps {
            font-size: 1.3rem;
        }
        .price {
            font-size: 1.5rem;
        }
    }

</style>