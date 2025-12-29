<script>
    export let message;
    export let color;
</script>

<div class="console"
    style="color: {color}">
    {message}
</div>

<style>
    .console{
        background-color: #2f2f2f;
        width:22rem;
        height: 15rem;
        padding: 1rem;
        border-radius: 0.5rem;
    }
</style>