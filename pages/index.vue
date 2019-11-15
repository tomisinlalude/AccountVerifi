<template>
    <main class="container">
      <h1>
        Welcome to AccountVerifi
      </h1>
      <h4>
        The most account number verification app on the web
      </h4>
      <button class="button is-medium is-primary is-rounded">
        Verify Account Number
      </button>
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
