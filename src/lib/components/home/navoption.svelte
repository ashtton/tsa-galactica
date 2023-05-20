<script>
    import {onMount} from "svelte";

    export let name;
    export let ref;
    export let tip;

    import Tooltip from "sv-tooltip"

    let screenSize;

    function updateScreenSize() {
        setTimeout(() => {
            screenSize = window.screen.width
            updateScreenSize()
        }, 1000)
    }

    onMount(() => {
        screenSize = window.screen.width;
        updateScreenSize()
    })
</script>

{#if screenSize > 800}
    <Tooltip tip={tip} top>
        <a href="/info/{ref}" class="option">
            <div class="image">
                <slot />
            </div>
            <div class="desc">
                <p>{name}</p>
            </div>
        </a>
    </Tooltip>
{:else}
    <a href="/info/{ref}" class="option">
        <div class="image">
            <slot />
        </div>
        <div class="desc">
            <p>{name}</p>
        </div>
    </a>
{/if}



<style>
    .image {
        height: 128px;
        width: 128px;
    }

    .option {
        color: #9a9a9a;
        transition: all .2s ease-in-out;
        display: flex;
        flex-direction: column;
        align-items: center;
        cursor: pointer;
        justify-content: center;
        user-select: none;
    }

    .option:hover {
        scale: 150%;
        color: white;
    }

    .desc {
        font-weight: bold;
        display: flex;
        align-items: center;
    }
</style>