<script>
    import IoIosWifi from 'svelte-icons/io/IoIosWifi.svelte'
    import IoMdPizza from 'svelte-icons/io/IoMdPizza.svelte'
    import IoIosEgg from 'svelte-icons/io/IoIosEgg.svelte'
    import IoIosLaptop from 'svelte-icons/io/IoIosLaptop.svelte'
    import GiCardJoker from 'svelte-icons/gi/GiCardJoker.svelte'
    import FaFantasyFlightGames from 'svelte-icons/fa/FaFantasyFlightGames.svelte'
    import GiChipsBag from 'svelte-icons/gi/GiChipsBag.svelte'
    import GiTShirt from 'svelte-icons/gi/GiTShirt.svelte'
    import GiVacuumCleaner from 'svelte-icons/gi/GiVacuumCleaner.svelte'
    import FaToiletPaper from 'svelte-icons/fa/FaToiletPaper.svelte'
    import IoIosMedkit from 'svelte-icons/io/IoIosMedkit.svelte'

    import {page} from "$lib/page_store.js";
    page.set("Planning")
</script>

<section class="animate__animated animate__fadeIn">
    <p class="title">Planning</p>
    <p class="subtitle">Learn what we provide and what you should provide.</p>

    <div class="provided">
        <div class="animate__animated animate__delay-1s animate__fadeIn" style="--animate-delay: 0.5s;">
            <p class="title">What we provide:</p>
            <div class="list">
                <br><div class="list-o"><div class="header"><div class="icon"><IoIosWifi /></div>Wi-Fi</div>We provide high speed internet to all our astronauts.</div><br>
                <div><div class="header"><div class="icon"><FaToiletPaper /></div>Toiletries</div>Toiletries are provided in each of the rooms.</div><br>
                <div><div class="header"><div class="icon"><IoIosEgg /></div>Breakfast</div>We serve Breakfast from 7:00 - 11:00 AM daily.</div><br>
                <div><div class="header"><div class="icon"><IoMdPizza /></div>Dinner</div>We serve Dinner from 5:00 - 7:00 PM daily.</div><br>
                <div><div class="header"><div class="icon"><GiVacuumCleaner /></div>Cleaning</div>Rooms are cleaned every two days by our maids.</div><br>
                <div><div class="header"><div class="icon"><GiTShirt /></div>Laundry</div>There are laundry services available.</div><br>
                <div><div class="header"><div class="icon"><IoIosMedkit /></div>Hospital</div>All of your medical needs can be taken care of.</div><br>
            </div>
        </div>
        <div class="animate__animated animate__delay-2s animate__fadeIn" style="--animate-delay: 0.5s;">
            <p class="title">What you might want to bring:</p>
            <div class="list">
                <br><div class="list-o"><div class="header"><div class="icon"><IoIosLaptop /></div>Laptop</div>Bring a laptop so that you can keep up with Earth.</div><br>
                <div class="list-o"><div class="header"><div class="icon"><GiCardJoker /></div>Cards</div>Cards are fun for the whole family.</div><br>
                <div class="list-o"><div class="header"><div class="icon"><FaFantasyFlightGames /></div>Board Games</div>Not a fan of cards? Bring other board games for fun.</div><br>
                <div class="list-o"><div class="header"><div class="icon"><GiChipsBag /></div>Snacks</div>Make sure you bring snacks in case you get hungry.</div><br>
            </div>
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

    .provided {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }

    .header {
        display: flex;
        font-weight: bold;
        align-items: center;
        gap: 0.3rem;
        font-size: 1.5rem;
    }

    .icon {
        width: 32px;
        height: 32px;
    }
</style>
