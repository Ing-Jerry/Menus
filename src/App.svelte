<script>
  const menu = [
    {
      categoria: "☕ Cafés",
      items: [
        {
          nombre: "Café Americano",
          descripcion: "Clásico café negro",
          precio: 30
        },
        {
          nombre: "Capuccino",
          descripcion: "Espuma cremosa",
          precio: 45
        }
      ]
    },
    {
      categoria: "🥐 Panadería",
      items: [
        {
          nombre: "Croissant",
          descripcion: "Mantequilla recién horneado",
          precio: 35
        },
        {
          nombre: "Pan de chocolate",
          descripcion: "Relleno dulce",
          precio: 40
        }
      ]
    }
  ];
</script>

<main>
  <h1>☕ Café Demo</h1>

  {#each menu as categoria}
    <section>
      <h2>{categoria.categoria}</h2>

      {#each categoria.items as item}
        <div class="card">
          <div>
            <h3>{item.nombre}</h3>
            <p>{item.descripcion}</p>
          </div>
          <span>${item.precio}</span>
        </div>
      {/each}

    </section>
  {/each}
</main>

<style>
  main {
    max-width: 500px;
    margin: auto;
    font-family: system-ui;
    padding: 20px;
    background: #fafafa;
  }

  h1 {
    text-align: center;
    margin-bottom: 20px;
  }

  h2 {
    margin-top: 25px;
    border-bottom: 2px solid #ddd;
    padding-bottom: 5px;
  }

  .card {
    display: flex;
    justify-content: space-between;
    padding: 12px 0;
    border-bottom: 1px solid #eee;
  }

  h3 {
    margin: 0;
  }

  p {
    margin: 4px 0;
    color: #666;
    font-size: 14px;
  }

  span {
    font-weight: bold;
    color: #333;
  }
</style>