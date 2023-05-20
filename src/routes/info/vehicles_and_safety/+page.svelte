<script>
    import {page} from "$lib/page_store.js";
    page.set("Vehicles and Safety")
</script>

<section class="animate__animated animate__fadeIn">
    <div class="vehicles">
        <p class="title">Vehicles</p>
        <p class="subtitle">Take a look at the vehicles used on the trip.</p>
    </div>
    <div class="safety">
        <p class="title">Safety Information</p>
        <p class="subtitle">Take a look at this safety information.</p>
    </div>
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

