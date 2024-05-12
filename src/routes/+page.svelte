<script>
    import Layout from "../components/+layout.svelte";
    import Circle from "../components/circle/+circle.svelte";
    import Time from "../components/time/+time.svelte";

    let isShow = false;
    let openTimeModal = false;

    function handleShow() {
        isShow = !isShow;
    }

    function handleTimeModal() {
        openTimeModal = !openTimeModal;
    }
</script>

<Layout title="memory game">
    <div class="body">
        <div class="circle-container">
            {#each { length: 4 } as _, i}
                <div class="circle-mini-container">
                    {#each { length: 4 } as _, j}
                        <Circle value="test" show={isShow} click={handleShow} />
                    {/each}
                </div>
            {/each}
        </div>
        <div class="player-container">
            <Time value="10:100" click={handleTimeModal} />
        </div>
    </div>
</Layout>

<style>
    .body {
        padding-top: 40px;
        display: flex;
        flex-direction: column;
        align-items: center;
        height: 100vh;
    }
    .circle-mini-container {
        display: flex;
        width: 80%;
        display: flex;
        justify-content: center;
        height: 80%;
    }
    .circle-container {
        width: 55%;
        height: 60%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .player-container {
        padding-top: 40px;
        display: flex;
        width: 55%;
    }
</style>
