<template>
  <div id="app">
    <nav class="nav">
      <header class="Header_container">
        <div class="Header_nav_lf">
          <nuxt-link :to="{path: '/', params: {}}">Info4u</nuxt-link>
          <nuxt-link :to="{path: '/mobile', params: {}}">mobile</nuxt-link>
          <nuxt-link :to="{path: '/news', params: {}}">news</nuxt-link>
        </div>
        <div class="Header_nav_rt"></div>
      </header>
    </nav>
    <div class="nav__placeholder"></div>
    <nuxt />
  </div>
</template>
