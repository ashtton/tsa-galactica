<script>
    import NavOption from '$lib/components/home/navoption.svelte'
    import IoIosPricetags from 'svelte-icons/io/IoIosPricetags.svelte'
    import IoIosCalendar from 'svelte-icons/io/IoIosCalendar.svelte'
    import IoIosBicycle from 'svelte-icons/io/IoIosBicycle.svelte'
    import IoIosCar from 'svelte-icons/io/IoIosCar.svelte'
    import IoMdRocket from 'svelte-icons/io/IoMdRocket.svelte'
</script>

<section>
    <div class="container">
        <div class="header animate__animated animate__fadeInDown">
            <div class="title">
                GALACTICA
            </div>
            <div class="subtitle">
                Space Tourism - The Right Way
            </div>
        </div>

        <div class="options animate__animated animate__delay-1s animate__fadeIn">
            <NavOption
                    name="Pricing"
                    ref="pricing"
                    tip="Use our pricing calculator to determine<br> how much your trip will cost."
            >
                <IoIosPricetags />
            </NavOption>
            <NavOption
                    name="Planning"
                    ref="planning"
                    tip="Plan your trip to become an astronaut."
            >
                <IoIosCalendar />
            </NavOption>
            <NavOption
                    name="Training"
                    ref="training"
                    tip="Learn about what you will need<br> to know to go on the trip."
            >
                <IoIosBicycle />
            </NavOption>
            <div class="break"></div>
            <NavOption
                    name="Vehicles & Safety"
                    ref="vehicles_and_safety"
                    tip="The vehicle and safety information for the trip.">
                <IoIosCar />
            </NavOption>
            <NavOption
                    name="Launch & Recovery"
                    ref="launch_and_recovery"
                    tip="Learn about how the rocket launches<br> and how we recover it.">
                <IoMdRocket />
            </NavOption>
        </div>
    </div>
</section>

<style>
    .header {
        text-align: center;
        margin: 5rem 0;
    }

    .title {
        letter-spacing: 0.9rem;
        font-size: 5rem;
    }

    .subtitle {
        font-size: 2rem;
        color: #cccccc;
    }

    .options {
        display: flex;
        justify-content: center;
        column-gap: 5rem;
        row-gap: 1rem;
        flex-wrap: wrap;
    }

    .break {
        flex-basis: 100%;
        height: 0;
    }

    @media(max-width: 610px) {
        .title {
            font-size: 3rem;
        }
        .subtitle {
            font-size: 1.5rem;
        }
        .header {
            margin: 1rem 0;
        }

        .break {
            position: absolute;
        }
    }

    @media(max-width: 400px) {
        .title {
            font-size: 2rem;
        }

        .subtitle {
            font-size: 1.5rem;
        }
    }

    @media(max-width: 360px) {
        .subtitle {
            font-size: 1.25rem;
        }
    }

</style>