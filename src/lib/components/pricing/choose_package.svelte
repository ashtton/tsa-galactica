<script>
    import IoIosRocket from 'svelte-icons/io/IoIosRocket.svelte'
    import IoIosTrophy from 'svelte-icons/io/IoIosTrophy.svelte'
    import IoMdFlash from 'svelte-icons/io/IoMdFlash.svelte'
    import IoMdArrowDropright from 'svelte-icons/io/IoMdArrowDropright.svelte'

    import {chosenPackage} from "$lib/stores/pricing_store.js";
    import {goto} from "$app/navigation";

    function updatePackage(name, price) {
        let beforeValue = $chosenPackage;

        chosenPackage.set({
            name: name,
            price: price
        })

        if (beforeValue === undefined) {
            goto("#price")
        }
    }
</script>

<div id="choose-package" class="step animate__animated animate__fadeInDown">
    <div class="title">
        Step #2 - Choose a package
    </div>
    <div class="packages">
        <div class="package {$chosenPackage !== undefined && $chosenPackage.name === 'standard' ? 'selected' : ''}" on:click={() => updatePackage('standard', 0)}>
            <div class="icon"><IoIosRocket /></div>
            <div class="package-title">Standard</div>
            <div class="cost">+ $0</div>
            <div class="details">
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Basic toiletries are provided</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Access to the television</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Internet access through Wi-Fi</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Hotel room with 1-2 beds</div>
            </div>
        </div>

        <div class="package {$chosenPackage !== undefined && $chosenPackage.name === 'premium' ? 'selected' : ''}" on:click={() => updatePackage('premium', 1000)}>
            <div class="icon"><IoIosTrophy /></div>
            <div class="package-title">Premium</div>
            <div class="cost">+ $1,000</div>
            <div class="details">
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Basic toiletries are provided</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Access to the television</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Buffet provided during dinner</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Netflix Provided</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Internet access through Wi-Fi</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Hotel room with 2-3 beds</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Access to the training room</div>
            </div>
        </div>

        <div class="package {$chosenPackage !== undefined && $chosenPackage.name === 'supreme' ? 'selected' : ''}" on:click={() => updatePackage('supreme', 5000)}>
            <div class="icon"><IoMdFlash /></div>
            <div class="package-title">Supreme</div>
            <div class="cost">+ $5,000</div>
            <div class="details">
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Basic toiletries are provided</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Access to the television</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Buffet provided during dinner</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Netflix + Hulu + Disney Plus </div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>High speed internet access</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>A full suite of rooms</div>
                <div class="detail"><div class="arrow"><IoMdArrowDropright /></div>Access to the training room</div>
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
        user-select: none;
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

    .detail {
        display: flex;
        align-items: center;
    }

    .arrow {
        width: 24px;
        height: 24px;
    }

</style>