<template>
  <main class="container verify-section">
    <h2>Verify Account Number</h2>
    <Form :banks="banks" />
  </main>
</template>

<script>
import Form from "~/components/Form.vue";
export default {
  head() {
    return {
      title: "AccountVerifi: Verify",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Most efficient way to verify your account number"
        }
      ]
    };
  },
  components: {
    Form
  },
  data() {
    return {
      banks: []
    };
  },
  mounted() {
    this.getBanks();
  },
  methods: {
    async getBanks() {
      const res = await fetch(`https://api.paystack.co/bank`, {
        method: "GET",
        headers: {
          "Content-Type": "application/json",
          Authorization: "sk_test_35fbc74be953bcb9297994032efcb28e9de4977d"
        }
      });
      if (res.ok) {
        const { data } = await res.json();
        return (this.banks = data);
      }
    }
  }
};
</script>

<style lang="scss" scoped>
@import "~/assets/scss/main.scss";
</style>
