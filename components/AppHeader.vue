<template>
<nav class="navbar container" role="navigation" aria-label="main navigation">
  <section class="navbar-brand">
    <nuxt-link class="navbar-item" to="/">
        <h1><span>Account</span>Verifi</h1>
    </nuxt-link>

    <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="appNavbar">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </section>

  <section id="appNavbar" class="navbar-menu">
    <section class="navbar-start">

      <nuxt-link class="navbar-item" to="/about">
        About
      </nuxt-link>
    </section>

    <section class="navbar-end">
      <section class="navbar-item">
          <nuxt-link class="button is-rounded is-primary is-small" to="/verify">
            Verify
          </nuxt-link>
      </section>
    </section>
  </section>
</nav>
</template>

<script>
export default {
    name: 'AppHeader'
}
</script>

<style lang="scss" scoped>
@import "~/assets/scss/main.scss";
</style>