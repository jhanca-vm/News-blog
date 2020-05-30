<script>
  export let segment;
</script>

<style>
  header nav {
    height: 100px;
    background: white;
    box-shadow: none;
  }

  nav .brand-logo {
    height: 100px;
    left: 15%;
  }
  
  nav .brand-logo img {
    width: 52px;
  }

  nav ul {
    height: 100px;
  }

  nav ul a {
    color: grey;
  }
</style>

<header>
  <nav class="container">
    <a class="brand-logo valign-wrapper" aria-current='{segment === undefined ? "page" : undefined}' href='.'>
      <img class="responsive-img left z-depth-2" src="Logo.jpg" alt="Logo">
    </a>
    <ul class="right valign-wrapper">
      <li>
        <a href="/">Sobre nosotros</a>
      </li>
      <li>
        <a href="/">Contacto</a>
      </li>
      <li>
        <a class="btn teal darken-2 white-text" href="/">Registro</a>
      </li>
    </ul>
  </nav>
</header>