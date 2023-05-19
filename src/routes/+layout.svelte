<script>
    import Particles from "svelte-particles";
    import {loadFull} from "tsparticles";

    let conf = {
        "particles": {
            "number": {
                "value": 300,
                "density": {
                    "enable": true,
                    "value_area": 473.51100518494565
                }
            },
            "color": {
                "value": "#ffffff"
            },
            "shape": {
                "type": "star",
                "stroke": {
                    "width": 0,
                    "color": "#000000"
                },
                "polygon": {
                    "nb_sides": 5
                }
            },
            "opacity": {
                "value": 1,
                "random": true,
                "anim": {
                    "enable": false,
                    "speed": 1,
                    "opacity_min": 0,
                    "sync": false
                }
            },
            "size": {
                "value": 2.1,
                "random": true,
                "anim": {
                    "enable": false,
                    "speed": 75.4716981132076,
                    "size_min": 0.3,
                    "sync": false
                }
            },
            "line_linked": {
                "enable": false,
                "distance": 150,
                "color": "#ffffff",
                "opacity": 0.4,
                "width": 1
            },
            "move": {
                "enable": true,
                "speed": 0.2,
                "direction": "none",
                "random": false,
                "straight": true,
                "out_mode": "bounce",
                "bounce": false,
                "attract": {
                    "enable": false,
                    "rotateX": 600,
                    "rotateY": 600
                }
            }
        },
        "retina_detect": true
    };

    let particlesInit = async main => {
        await loadFull(main);
    };

    import {page} from "$lib/page_store.js";
</script>

<svelte:head>
    <title>Galactica - {$page}</title>
</svelte:head>

<main>
    <slot />
</main>

<Particles
        id="particles"
        options={conf}
        particlesInit="{particlesInit}"
/>

<style>
    :global(body) {
        color: white;
        background-color: black;
        font-family: arial;
        margin: 0;
    }

    :global(a) {
        text-decoration: none;
    }

    :global(a):visited {
        color: inherit;
    }

    :global(p) {
        margin: 0;
    }
</style>