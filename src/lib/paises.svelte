<script>
  import colImg from '../assets/colombia.png.jpg';
  import venImg from '../assets/venezuela.png.png';
  import ecuImg from '../assets/ecuador.png.png';
  import perImg from '../assets/peru.png.png';
  import braImg from '../assets/brasil.png.png';

  export let pais;
  let p;

  const paises = {
    colombia: ["Colombia", "Bogotá", "51,52 millones", "Peso colombiano", "1.142.000 km²", colImg],
    venezuela: ["Venezuela", "Caracas", "28,2 millones", "Bolívar", "916.445 km²", venImg],
    ecuador: ["Ecuador", "Quito", "17,8 millones", "Dólar estadounidense", "256.370 km²", ecuImg],
    peru: ["Perú", "Lima", "33,72 millones", "Sol peruano", "1.285.215 km²", perImg],
    brasil: ["Brasil", "Brasília", "214,3 millones", "Real brasileño", "8.510.000 km²", braImg]
  };

  p = paises[pais];
</script>

<div class="main">
  <div class="col1">
    <img src={p[5]} alt={`Bandera de ${p[0]}`} width="300" height="200" />
  </div>
  <div class="col2">
    <div class="linea"><strong>País:</strong> {p[0]}</div>
    <div class="linea"><strong>Capital:</strong> {p[1]}</div>
    <div class="linea"><strong>Población:</strong> {p[2]}</div>
    <div class="linea"><strong>Moneda:</strong> {p[3]}</div>
    <div class="linea"><strong>Extensión:</strong> {p[4]}</div>
  </div>
</div>

<style>
  .main {
    align-items: center;
    border: 1px solid #dce8df;
    border-radius: 16px;
    background: #fff;
    display: grid;
    gap: 16px;
    grid-template-columns: minmax(110px, 0.8fr) minmax(0, 1.2fr);
    min-width: 0;
    padding: 14px;
    box-shadow: 0 8px 24px rgb(27 68 45 / 8%);
    transition: transform 160ms ease, box-shadow 160ms ease;
  }

  .main:hover {
    transform: translateY(-2px);
    box-shadow: 0 12px 28px rgb(27 68 45 / 13%);
  }

  .col1 img {
    display: block;
    width: 100%;
    height: 118px;
    border-radius: 10px;
    object-fit: cover;
  }

  .col2 {
    min-width: 0;
  }

  strong {
    color: #16835d;
    font-weight: 700;
  }

  .linea {
    margin: 0 0 8px;
    color: #34473d;
    font-size: 0.92rem;
    line-height: 1.35;
  }

  .linea:last-child {
    margin-bottom: 0;
  }

  @media (max-width: 420px) {
    .main {
      grid-template-columns: 1fr;
    }

    .col1 img {
      height: 160px;
    }
  }
</style>