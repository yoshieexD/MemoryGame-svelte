<script>
    export let value;
    export let show = false;
    export let click;
</script>

<button class="circle-layout" on:click={click}>
    {value}
    {show}
</button>

<style>
    .circle-layout {
        background-color: rgb(37, 37, 67);
        border-radius: 50%;
        width: 17%;
        height: 90%;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        margin: 10px;
        border: 0;
        cursor: pointer;
    }
</style>
