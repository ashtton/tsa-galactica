<script>
    import {page} from "$lib/page_store.js";
    page.set("resources")
</script>

<section class="animate__animated animate__fadeIn">
    <p class="title">Resources Used</p>
    <p class="subtitle">These are the resources used to create this website.</p>
    <div class="info">
        <div>
            <p class="title">TSA Documents:</p>
            <ul style="font-size: 1.2rem;">
                <li class="link"><a href="/docs/Worklog.pdf" target="_blank">Worklog</a></li>
                <li class="link"><a href="/docs/CopyrightChecklist.pdf" target="_blank">Copyright Checklist</a></li>
            </ul>
        </div>
        <div>
            <p class="title">Information Resources:</p>
            <ul style="font-size: 1.2rem;">
                <li class="link"><a href="https://global.jaxa.jp/" target="_blank">Jaxa</a></li>
                <li class="link"><a href="https://www.nasa.gov/" target="_blank">Nasa</a></li>
                <li class="link"><a href="https://www.faasafety.gov/" target="_blank">Faasafety</a></li>
                <li class="link"><a href="https://www.britannica.com/" target="_blank">Britannica</a></li>
            </ul>
        </div>
        <div>
            <p class="title">Development Resources:</p>
            <ul style="font-size: 1.2rem;">
                <li class="link"><a href="https://kit.svelte.dev/" target="_blank">Svelte Kit</a></li>
                <li class="link"><a href="https://svelte-icons.vercel.app/" target="_blank">Svelte Icons</a></li>
                <li class="link"><a href="https://particles.js.org/" target="_blank">Particles JS</a></li>
                <li class="link"><a href="https://animate.style/" target="_blank">Animate CSS</a></li>
            </ul>
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

    .info {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }

    .link {
        color: gray;
    }

    .link:hover {
        color: white;
    }
</style>
