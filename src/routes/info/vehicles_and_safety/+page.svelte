<script>
    import {page} from "$lib/page_store.js";
    page.set("Vehicles and Safety")
</script>

<section class="animate__animated animate__fadeIn">
    <div class="vehicles">
        <p class="title">Vehicles</p>
        <p class="subtitle">Take a look at the vehicles used on the trip.</p>
        <div>
            <div class="animate__animated animate__delay-1s animate__fadeIn" style="--animate-delay: 0.5s">
                <p class="title">SC-404</p>
                <p style="font-size: 1.2rem">Our only rocket ready for take-off which is named the SC-404. Being made out of Graphite-epoxy, it is
                super durable and resistant to heat elements, which allows for a safe exit and re-entry from Earth. Holding up
                to 900 people per cruiser, we have 15 public decks, 7 Tier One decks which include the standard hotels. Each
                deck has their own kitchen. 4 Tier Two decks which include the premium hotels, training rooms, and each with
                their own buffet. Finally, our 4 Tier Three Decks, which include the suites, training rooms, indoor theater, and
                buffets.</p>
            </div>
        </div>
    </div>
    <div class="safety">
        <p class="title animate__animated animate__delay-1s animate__fadeIn">Safety Information</p>
        <p class="subtitle animate__animated animate__delay-1s animate__fadeIn">Take a look at this safety information.</p>
        <div class="animate__animated animate__delay-3s animate__fadeIn" style="--animate-delay: 0.5s">
            <ol style="font-size: 1.2rem">
                <li>Each room is equipped with it's own safety pod.</li>
                <li>Fire extinguishers are located in every room.</li>
                <li>The ship is fully equipped with fire/carbon monoxide detectors.</li>
                <li>There will be a pre-takeoff briefing of the whole ship.</li>
                <li>The hospital suite is equipped with medical professionals.</li>
                <li>Extensive security measures are taken with a large team.</li>
            </ol>
        </div>
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

