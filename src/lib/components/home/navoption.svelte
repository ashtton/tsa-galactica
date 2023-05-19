<script>
    export let name;
    export let ref;
    export let tip;

    import Tooltip from "sv-tooltip"
</script>

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