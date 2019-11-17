<template>
    <main class="container">
      <h1>
        Welcome to AccountVerifi
      </h1>
      <h4>
        The most trusted account number verification app on the web
      </h4>
      <nuxt-link to="/verify" class="button is-medium is-primary is-rounded main-button">
        Verify Account Number
      </nuxt-link>
    </main>
</template>

<script>

export default {
  head() {
    return {
      title: "AccountVerifi: Home",
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: "Most efficient way to verify your account number"
        }
      ]
    };
  }
}
</script>

<style lang="scss" scoped>
@import "~/assets/scss/main.scss";
</style>
