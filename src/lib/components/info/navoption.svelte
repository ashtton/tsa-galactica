<script>
    import {page} from "$lib/page_store.js";

    export let ref;
    export let name;

    import Tooltip from "sv-tooltip"
</script>

<Tooltip tip={name} bottom>
    <a href="/info/{ref}" class="option {$page.replaceAll(' ', '_').toLowerCase() === ref ? 'selected' : ''}">
        <div class="image">
            <slot />
        </div>
    </a>
</Tooltip>

<style>
    .image {
        height: 46px;
        width: 46px;
    }

    .option {
        color: #9a9a9a;
        transition: all .2s ease-in-out;
        display: flex;
        flex-direction: column;
        align-items: center;
        cursor: pointer;
        justify-content: center;
    }

    .option:hover, .selected {
        scale: 150%;
        color: white;
    }

    @media(max-width: 420px) {
        .image {
            height: 32px;
            width: 32px;
        }

    }
</style>