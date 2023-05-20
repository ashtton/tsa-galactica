<script>
    import IoIosRocket from 'svelte-icons/io/IoIosRocket.svelte'
    import IoIosTrophy from 'svelte-icons/io/IoIosTrophy.svelte'
    import IoMdFlash from 'svelte-icons/io/IoMdFlash.svelte'

    import {chosenPackage} from "$lib/stores/pricing_store.js";
</script>

<div class="step animate__animated animate__fadeInDown">
    <div class="title">
        Step #2 - Choose a package
    </div>
    <div class="packages">
        <div class="package {$chosenPackage !== undefined && $chosenPackage === 'standard' ? 'selected' : ''}" on:click={() => chosenPackage.set('standard')}>
            <div class="icon"><IoIosRocket /></div>
            <div class="package-title">Standard</div>
            <div class="cost">+ $0</div>
            <div class="details">
                <p>- Is a bananaa sdasdasasdas</p>
                <p>- Is a bananaa</p>
            </div>
        </div>

        <div class="package {$chosenPackage !== undefined && $chosenPackage === 'premium' ? 'selected' : ''}" on:click={() => chosenPackage.set('premium')}>
            <div class="icon"><IoIosTrophy /></div>
            <div class="package-title">Premium</div>
            <div class="cost">+ $1,000</div>
            <div class="details">
                <p>- Is a bananaa sdasdasasdas</p>
                <p>- Is a bananaa</p>
            </div>
        </div>

        <div class="package {$chosenPackage !== undefined && $chosenPackage === 'supreme' ? 'selected' : ''}" on:click={() => chosenPackage.set('supreme')}>
            <div class="icon"><IoMdFlash /></div>
            <div class="package-title">Supreme</div>
            <div class="cost">+ $5,000</div>
            <div class="details">
                <p>- Is a bananaa sdasdasasdas</p>
                <p>- Is a bananaa</p>
            </div>
        </div>
    </div>
</div>

<style>
    .title {
        font-weight: bold;
        font-size: 1.2rem;
        margin-bottom: 1rem;
        margin-top: 1.5rem;
    }

    .packages {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 1rem;
    }

    .package {
        border: 1px solid gray;
        color: gray;
        border-radius: 0.2rem;
        display: flex;
        flex-direction: column;
        text-align: center;
        align-items: center;
        cursor: pointer;
        padding: 0.5rem;
    }

    .package:hover, .selected {
        border-color: white;
        color: white;
        scale: 105%;
    }

    .icon {
        height: 100px;
        width: 100px;
    }

    .package-title {
        font-weight: bold;
        font-size: 1.2rem;
    }

    .cost {
        margin-bottom: 0.7rem;
    }

    .details {
        text-align: left;
    }

</style>