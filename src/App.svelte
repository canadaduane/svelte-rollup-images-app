<script>
  export let name;

  import settingsImage from "./images/settings.svg";

  import BigX from "./bigx/BigX.svelte";
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  img {
    width: $width;
  }
  .gear {
    margin: auto;
    width: 100px;
    height: 100px;
    background-color: #ccc;
    background-image: url(./images/settings.svg);
  }
</style>

<main>
  <h1>Hello {name}!</h1>
  <h2>Image source from javascript with global CSS variable used for width</h2>
  <p><img src={settingsImage} alt="gear" /></p>
  <h2>Image as CSS background-image url()</h2>
  <div class="gear" />
  <h2>Image as CSS background-image url() inside component</h2>
  <BigX />
</main>
