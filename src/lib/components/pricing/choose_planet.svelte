<script>
    import Planet from './planet.svelte'
    import {chosenPlanet} from "$lib/stores/pricing_store.js";
</script>

<div class="step">
    <div class="title">
        Step #1 - Choose a destination
    </div>
    <div class="planets">
        <Planet
                src="mercury"
                miles="62,454,000"
                time="294 Days"
                delay="100ms"
                price="377312.48"
        />
        <Planet
                src="venus"
                miles="77,782,000"
                time="218 Days"
                delay="200ms"
                price="469650.72"
        />
        <Planet
                src="mars"
                miles="177,460,000"
                time="336 Days"
                delay="400ms"
                price="1071763.68"
        />
        <Planet
                src="jupiter"
                miles="541,640,000"
                time="780 Days"
                delay="500ms"
                price="3270971.84"
        />
        <Planet
                src="saturn"
                miles="918,450,000"
                time="2,310 Days"
                delay="600ms"
                price="5546514.56"
        />
        <Planet
                src="uranus"
                miles="1,918,700,000"
                time="6,935 Days"
                delay="700ms"
                price="11587271.20"
        />
        <Planet
                src="neptune"
                miles="2,823,360,000"
                time="8,760 Days"
                delay="800ms"
                price="17051472.16"
        />
    </div>
</div>

<style>
    .title {
        font-weight: bold;
        font-size: 1.2rem;
        margin-bottom: 0.5rem;
    }

    .planets {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 1rem;
    }
</style>