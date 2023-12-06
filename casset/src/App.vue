<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark">
    <div class="container-fluid">
        <RouterLink to="/" class="navbar-brand text-primary"><img src="./assets/logo.svg" alt="logo" width="30px"><span class="px-2"><b>Casset</b></span></RouterLink>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav mr-auto">
                <li class="nav-item px-3">
                  <RouterLink to="/">Home</RouterLink>
                </li>
                <li class="nav-item px-3">
                  <RouterLink to="/about">About</RouterLink>
                </li>
            </ul>
        </div>
    </div>
  </nav>
  <header>
    
  </header>

  <RouterView />
</template>

<style scoped>

nav a.router-link-exact-active {
  color: var(--color-text);
  font-weight: bold;
}
</style>
