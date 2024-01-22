<script>
  export let props = {
    color1: "",
    color2: "",
    color3: "",
    gradientColor: "",
  };
</script>

<div class="grid-item">
  <div
    class="gradient-circle"
    style={`background-image: ${props.gradientColor}`}
  ></div>

  <div class="color-code--grid">
    <div class="colorAndCode">
      <div
        class="color-circle color1"
        style={`background-color: ${props.color1};`}
      ></div>
      <p>{props.color1}</p>
    </div>

    <div class="colorAndCode">
      <div
        class="color-circle color2"
        style={`background-color: ${props.color2};`}
      ></div>
      <p>{props.color2}</p>
    </div>

    <div class="colorAndCode">
      <div
        class="color-circle color3"
        style={`background-color: ${props.color3};`}
      ></div>
      <p>{props.color3}</p>
    </div>
  </div>
</div>

<style lang="scss">
  .grid-item {
    padding-top: 1.5em;
  }
  .gradient-circle {
    margin: 0 auto;
    width: clamp(70px, 14vw, 120px);
    height: clamp(70px, 14vw, 120px);
    border-radius: 50%;
    background-size: contain;
  }

  .color-code--grid {
    display: grid;
    place-items: center;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;

    .colorAndCode {
      margin-top: 1.5rem;
    }
  }

  .color-circle {
    width: clamp(25px, 6.5vw, 45px);
    height: clamp(25px, 6.5vw, 45px);
    border-radius: 50%;
    margin: 0 auto;
  }
</style>
