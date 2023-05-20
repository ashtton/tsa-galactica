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
        />
        <Planet
                src="venus"
                miles="77,782,000"
                time="218 Days"
                delay="200ms"
        />
        <Planet
                src="mars"
                miles="177,460,000"
                time="336 Days"
                delay="400ms"
        />
        <Planet
                src="jupiter"
                miles="541,640,000"
                time="780 Days"
                delay="500ms"
        />
        <Planet
                src="saturn"
                miles="918,450,000"
                time="2,310 Days"
                delay="600ms"
        />
        <Planet
                src="uranus"
                miles="1,918,700,000"
                time="6,935 Days"
                delay="700ms"
        />
        <Planet
                src="neptune"
                miles="2,823,360,000"
                time="8,760 Days"
                delay="800ms"
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