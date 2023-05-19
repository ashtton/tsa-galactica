<script>
    import NavOption from '$lib/components/info/navoption.svelte'
    import IoIosPricetags from 'svelte-icons/io/IoIosPricetags.svelte'
    import IoIosCalendar from 'svelte-icons/io/IoIosCalendar.svelte'
    import IoIosBicycle from 'svelte-icons/io/IoIosBicycle.svelte'
    import IoIosCar from 'svelte-icons/io/IoIosCar.svelte'
    import IoMdRocket from 'svelte-icons/io/IoMdRocket.svelte'
</script>
<section class="container animate__animated animate__fadeIn">
    <div class="header">
        <a class="title" href="/">GALACTICA</a>
        <div class="break"></div>
        <div class="options">
            <NavOption
                    name="Pricing"
                    ref="pricing"
            >
                <IoIosPricetags />
            </NavOption>
            <NavOption
                    name="Planning"
                    ref="planning"
            >
                <IoIosCalendar />
            </NavOption>

            <NavOption
                    name="Launch & Recovery"
                    ref="launch_and_recovery"
            >
                <IoMdRocket />
            </NavOption>
            <NavOption
                    name="Vehicles & Safety"
                    ref="vehicles_and_safety"
            >
                <IoIosCar />
            </NavOption>
            <NavOption
                    name="Training"
                    ref="training"
            >
                <IoIosBicycle />
            </NavOption>
        </div>
    </div>

    <div>
        <slot />
    </div>
</section>

<style>
    section {
        margin-top: 3rem;
    }

    .container {
        max-width: 800px;
        margin: auto;
    }

    .header {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 0.2rem;
        margin-top: 1rem;
    }

    .title {
        font-weight: bold;
        letter-spacing: 0.9rem;
        font-size: 3rem;
        text-align: center;
    }

    .options {
        display: flex;
        gap: 1rem;
    }

    .break {
        flex-basis: 100%;
        height: 0;
    }

    @media(max-width: 420px) {
        .title {
            font-size: 1.7rem;
        }
    }

</style>