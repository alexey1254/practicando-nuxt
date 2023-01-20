<template> <!--nuxtLink sive para que sea una SPA y no se recargue la pagina al hacer click en un href-->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <nuxtLink class="navbar-brand" to="/">Intro Nuxt</nuxtLink>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
            <nuxtLink class="nav-link active" aria-current="page" to="/">Inicio</nuxtLink>
        </li>
        <li class="nav-item">
            <nuxtLink class="nav-link active" aria-current="page" to="/home">Home</nuxtLink>
        </li>
        <li class="nav-item">
            <nuxtLink class="nav-link active" aria-current="page" to="/about">About</nuxtLink>
        </li>
        <li class="nav-item">
            <nuxtLink class="nav-link active" aria-current="page" to="/posts">Posts</nuxtLink>
        </li>
        <li class="nav-item">
            <nuxtLink class="nav-link active" aria-current="page" to="/pokeapi">Pokeapi</nuxtLink>
        </li>
      </ul>
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Buscar" aria-label="Buscar">
        <button class="btn btn-outline-success" type="submit">Buscar</button>
      </form>
    </div>
  </div>
</nav>
</template>