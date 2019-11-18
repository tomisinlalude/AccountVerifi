<template>
  <div>
    <div class="field">
      <div class="control">
        <input
          class="input input1 is-rounded is-normal"
          type="number"
          v-model="accountNumber"
          placeholder="Acount Number"
        />
        <div class="select is-rounded is-normal">
          <select class="select-field" v-model="bankCode">
            <option selected disabled value="">Select a Bank</option>
            <option v-for="bank in banks" :value="bank.code" :key="bank.id">{{
              bank.name
            }}</option>
          </select>
        </div>
      </div>
    </div>
    <div class="verify-reset">
      <button class="button is-primary is-rounded is-small" @click="validate">
        Verify
      </button>
      <button class="button is-primary is-rounded is-small" @click="reset">
        Reset
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["banks"],
  data() {
    return {
      accountNumber: "",
      bankCode: ""
    };
  },
  methods: {
    async validate() {
      const res = await fetch(
        `https://api.paystack.co/bank/resolve?bank_code=${this.bankCode}&account_number=${this.accountNumber}`,
        {
          method: "GET",
          headers: {
            "Content-Type": "application/json",
            Authorization: "Bearer sk_test_35fbc74be953bcb9297994032efcb28e9de4977d"
          }
        }
      );
      if (res.ok) {
        return alert("Account number successfully verified");
      }
      return alert("Invalid Account Number");
    },
    async reset() {
      this.bankCode = "";
      this.accountNumber = "";
    }
  }
};
</script>

<style lang="scss" scoped>
@import "~/assets/scss/main.scss";
</style>
