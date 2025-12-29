<script>
    export let label = "Button";
    export let checked = false;
</script>

<!--
<button
 class={checked ? "checked" : "unchecked"} onclick={OnClick}
>{label}</button>
-->
<button class="button-outline {checked ? "button-outline-checked" : "button-outline-unchecked"}" type="button" on:click>
  <div class="switch">
    {label}
  </div>
</button>


<style>
    .button-outline {
        display: inline-block;
        padding: 0.5rem;                 /* bezel thickness */
        background-color: #2f2f2f;        /* cockpit gray interior */
        border-radius: 0.15rem;
        transition:
            border-color 0.15s ease-out,
            box-shadow 0.15s ease-out;
    }
    .button-outline-unchecked {
        border: 0.4rem solid #6a6a6a;
        box-shadow: none;
    }
    .button-outline-checked {
        border: 0.4rem solid #66ff66;
        box-shadow:
            0 0 0.6rem rgba(102,255,102,0.7),
            0 0 1.4rem rgba(102,255,102,0.4),
            0 0 2.6rem rgba(102,255,102,0.2);
    }


    .switch {
        background-color: rgb(28,28,28);
        color: #b4f8b4;
        font-family: 'Orbitron', sans-serif;
        font-weight: bold;
        font-size: 1.5rem;
        text-transform: uppercase;
        letter-spacing: 0.05rem;
        cursor: pointer;

        /* Fixed hardware-style dimensions */
        width: 11rem;
        height: 9rem;

        /* Center label perfectly */
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;

        /* Prevent text from resizing the button */
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;

        /* 3D raised effect on all sides */
        box-shadow:
            0.4rem 0.4rem 0.4rem #0f0f0f,     /* bottom-right shadow */
        -0.2rem -0.2rem 0.4rem #373737,    /* top-left highlight */
            inset 0 -0.2rem 0.2rem rgba(0,0,0,0.3);

        transition: box-shadow 0.12s ease-out, background-color 0.12s ease-out;
    }
    .switch:active {
        box-shadow:
            0.1rem 0.1rem 0.2rem #111111,            /* bottom-right depth */
            -0.05rem -0.05rem 0.2rem #5a5a5a,         /* top-left highlight */
            inset 0.25rem 0.25rem 0.35rem rgba(0,0,0,0.75),
            inset -0.15rem -0.15rem 0.25rem rgba(255,255,255,0.05);
    }


</style>