<script>
    import Planet from './planet.svelte'
</script>

<div class="step">
    <div class="planets">
        <Planet
                src="mercury"
                delay="100ms"
        />
        <Planet
                src="venus"
                delay="200ms"
        />
        <Planet
                src="earth"
                delay="300ms"
        />
        <Planet
                src="mars"
                delay="400ms"
        />
        <Planet
                src="jupiter"
                delay="500ms"
        />
        <Planet
                src="saturn"
                delay="600ms"
        />
        <Planet
                src="uranus"
                delay="700ms"
        />
        <Planet
                src="neptune"
                delay="800ms"
        />
    </div>
</div>