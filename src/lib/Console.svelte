<script>
    export let message;
    export let color;
    let messages = message.split("\n");

</script>

<div class="console"
    style="color: {color}">
    <ul>
        {#each messages as line}
        <li>{line}</li>
        {/each}
    </ul>
    <span class="cursor">█</span>
</div>

<style>

    .console{
        background-color: #0b0f0c;
        font-family: 'DSEG14', monospace;
        font-size: 0.75rem;
        word-spacing: 0.5rem;
        line-height: 1.2rem;
        width:20rem;
        height: 15rem;
        padding: 1rem;
        border-radius: 0.5rem;
    }

    ul{
        list-style-type: none;
        padding: 0;
    }

    .cursor {
        display: inline-block;
        margin-left: 2px;
        width: 0.6ch;
        animation: blink 1s steps(2, start) infinite;
    }

    @keyframes blink {
        0%, 50% { opacity: 1; }
        50.01%, 100% { opacity: 0; }
    }           
    
</style>