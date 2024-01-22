<script lang="ts">
  import GradientGridItem from "./GradientGridItem.svelte";
  const gradientObjects = [
    {
      color1: "#000E1B",
      color2: "#091C2E",
      color3: "#D6A994",
      gradientColor: "linear-gradient(to bottom, #000e1b, #091C2E, #d6a994)",
    },
    {
      color1: "#000B00",
      color2: "#4A5885",
      color3: "#FBFAF5",
      gradientColor: "linear-gradient(to bottom, #010101, #495883, #D3D0CB)",
    },
    {
      color1: "#222940",
      color2: "#D32F30",
      color3: "#B3B2AE",
      gradientColor: "linear-gradient(to bottom, #222940, #D32F30, #B3B2AE)",
    },
    {
      color1: "#180614",
      color2: "#C099A0",
      color3: "#E4D2D8",
      gradientColor: "linear-gradient(to bottom, #180614, #C099A0, #E4D2D8)",
    },
    {
      color1: "#16160E",
      color2: "#6C848D",
      color3: "#E6D190",
      gradientColor: "linear-gradient(to bottom, #16160E, #6C848D, #E6D190)",
    },
  ];
</script>

<div class="grid-container">
  {#each gradientObjects as go}
    <GradientGridItem props={go} />
  {/each}
</div>

<style lang="scss">
  .grid-container {
    display: grid;

    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    place-items: center;
    gap: 2rem;
  }
</style>
