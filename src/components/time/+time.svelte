<script>
    export let value;
    export let click;
</script>

<button class="time-container" on:click={click}>
    <p class="time">Time:</p>
    <p class="value">{value}</p>
</button>

<style>
    .time-container {
        background-color: rgb(224, 224, 226);
        display: flex;
        border: 0;
    }
</style>
