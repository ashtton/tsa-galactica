<script>
    let guidelines = "https://tsaweb.org/docs/default-source/themes-and-problems-2018-2019/2022-2023/hs---webmaster.pdf?sfvrsn=9d75e16c_2";
</script>
<footer class="container animate__animated animate__delay-1s animate__fadeInUp">
    <div class="footer">
        <div class="copyright animate__animated">© 2023 Galactica Inc.</div>
        <div class="links">
            <a class="link" href="/info/resources">Resources</a> <span>|</span>
            <a class="link" target="_blank" href="https://github.com/ashtton/tsa-galactica" >Github</a> <span>|</span>
            <a class="link" target="_blank" href="{guidelines}">TSA Guidelines</a>
        </div>
    </div>
</footer>

<style>
    .container {
        width: 100%;
        height: 5rem;
        background-color: black;
        z-index: 1000;
    }

    .footer {
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 100%;
        margin: auto;
        max-width: 800px;
    }

    .links {
        user-select: none;
    }

    .link {
        color: gray;
    }

    .link:hover {
        color: white;
    }

    .copyright {
        font-weight: bold;
    }

    @media(max-width: 800px) {
        .footer {
            margin-left: 1rem;
            margin-right: 1rem;
        }
    }
</style>