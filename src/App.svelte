<script>
  import Button from "./lib/Button.svelte";
  import Console from "./lib/Console.svelte";

  let isOn = $state(false);
  let BedroomOnClick = function () {
    isOn = !isOn;
  };

  let message = "Hello world this is\n what the font is";
  let showConsole = $state(false);
</script>

<div id="background">
  <div id="one-one">
    <Button label="Bedroom"
          checked={isOn}
          on:click={BedroomOnClick}></Button>
  </div>
  <div id="one-two">
    <Button label="Lamp"
          checked={isOn}
          on:click={() => showConsole = !showConsole}></Button>
  </div>
  <div id="three-three">
    {#if showConsole}
    <Console color="green" message={message}></Console>
    {/if}
  </div>
  
</div>

<style>
  #background{
    background-color: black; 
    width: 100vw; /* 100% view width */
    height: 100vh; /* 100% view width */
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(3, 1fr);

    place-items: center;
  }

  #one-one{
    grid-column: 1;
    grid-row: 1;
  }
  #one-two{
    grid-column: 2;
    grid-row: 1;
  }
  #three-three{
    grid-column: 4;
    grid-row: 3;
  }
</style>

