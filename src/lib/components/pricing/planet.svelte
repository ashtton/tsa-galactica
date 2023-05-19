<script>
    import Tooltip from "sv-tooltip";

    export let src;
    export let delay;
</script>

<Tooltip tip="Mercury<br>1500 Miles<br>$159195">
    <img alt="{src}" style="--animate-delay: {delay}" class="planet animate__animated animate__fadeIn animate__delay-1s" height="72px" src="/images/planets/{src}.png">
</Tooltip>
<style>
    .planet {
        filter: grayscale(100%);
    }

    .planet:hover {
        scale: 125%;
        transition: all .2s ease-in-out;
        filter: none;
    }
</style>