<template>
    <div>
        <nav class="navbar navbar-expand-lg bg-primary" data-bs-theme="dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/about">about me</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/limitmessage">Limit Message</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/previewImage">Preview Image</a>
        </li>
      </ul>
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav>
    </div>
    <slot />
    <footer class="mt-2">
        <nav data-bs-theme="dark">
        <div class="card text-center">
        <div class="card-header">
        Footer
        </div>
        <div class="card-body">
        <h5>TATC</h5>
        <h5 class="card-title">Adipat Sompong</h5>
        <p class="card-text">66309010019 IT.4/1</p>
        </div>
        </div>
        </nav>  
    </footer>
</template>
<style>

</style>