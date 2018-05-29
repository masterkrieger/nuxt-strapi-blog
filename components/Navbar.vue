<template>
  <div id="navbar">
    <nav class="navbar is-info" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="/"><strong>Blog Home</strong></a>
        <button class="button navbar-burger">
          <span></span>
          <span></span>
          <span></span>
        </button>
      </div>
      <div class="navbar-menu">
        <div class="navbar-end">
          <nuxt-link class="navbar-item" to="/about">About</nuxt-link>
          <!--
          <nuxt-link class="navbar-item" to="/projects">Projects</nuxt-link>
          <nuxt-link class="navbar-item" to="/contact">Contact</nuxt-link>
          -->
        </div>
      </div>
    </nav>
  </div>
</template>

<style>

  .navbar {
    background-color: #209cee; 
  }
  .navbar-item {
    color: #ffffff;
  }
</style>