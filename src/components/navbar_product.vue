<template>
<nav class="navbar navbar-expand-lg bg-warning p-3" data-bs-theme="dark"  >
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Shoping
    </a>
    <img src="https://wallpaperaccess.com/full/168399.jpg" alt="">
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <routerLink to="/" class="nav-link" aria-current="page">Home </routerLink>
        </li>
        <li class="nav-item">
          <routerLink to="/cart" class="nav-link" aria-current="page">สินค้า</routerLink>
        </li>
      </ul>
      
    </div>
  </div>
</nav>
</template>

<script setup>
import { useProductStore } from '../store/product';

const product_store = useProductStore()

</script>

<style lang="scss" scoped>

img{
  max-width: 60px;
  max-height: 60px;
}

</style>