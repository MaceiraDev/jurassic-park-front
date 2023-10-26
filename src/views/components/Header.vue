<template>
  <header>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
      <div class="container-fluid">
        <a class="navbar-brand" href="#"><img id="icon_header" src="./../../../public/images/icon_skull.png" /></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="/">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="/">Carnívoros</a>
            </li>
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="/">Herbíveros</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>
<script>
export default {
  setup() {

  },
}
</script>
<style scoped>
nav {
  background-color: #ded6c9 !important;
  padding: 10px;
}

.nav-link {
  color: #452b34 !important;
  transition: 0.3s;
  font-weight: 900;
}

.nav-link:hover {
  color: #c90a00 !important;
}

#icon_header {
  width: 50px;
  height: 50px;
}
</style>