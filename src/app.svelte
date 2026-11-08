<script>
  import Paises from './lib/paises.svelte';
</script>

<main class="container">
  <header class="intro">
    <p class="eyebrow">Explora el continente</p>
    <h1>Países de <span>Suramérica</span></h1>
    <p class="description">Conoce sus capitales, monedas, población y extensión.</p>
  </header>

  <section class="countries" aria-label="Países de Suramérica">
    <Paises pais="colombia" />
    <Paises pais="venezuela" />
    <Paises pais="ecuador" />
    <Paises pais="peru" />
    <Paises pais="brasil" />
  </section>
</main>

<style>
  .container {
    width: min(1120px, 100%);
    margin: 0 auto;
    padding: 64px 24px;
    box-sizing: border-box;
  }

  .intro {
    margin-bottom: 36px;
    text-align: center;
  }

  .eyebrow {
    margin: 0 0 8px;
    color: #16835d;
    font-size: 0.8rem;
    font-weight: 800;
    letter-spacing: 0.14em;
    text-transform: uppercase;
  }

  h1 {
    margin: 0;
    color: #18352b;
    font-size: clamp(2.3rem, 6vw, 4rem);
    line-height: 1.1;
  }

  h1 span {
    color: #16835d;
  }

  .description {
    margin: 14px 0 0;
    color: #60736a;
    font-size: 1.05rem;
  }

  .countries {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(min(100%, 440px), 1fr));
    gap: 18px;
  }

  @media (max-width: 600px) {
    .container {
      padding: 40px 16px;
    }

    .intro {
      margin-bottom: 28px;
    }
  }
</style>