
<template>
    <main class="container verify-section">
        <h2>Verify Account Number</h2>
        <form>
            <div class="field">
                <div class="control">
                    <input class="input input1 is-rounded is-normal" type="number" placeholder="Acount Number">
                    <div class="select is-rounded is-normal">
                        <select class="select-field">
                        <option value="">Select Bank</option>
                        <option value="access">Access Bank</option>
                        <option value="citibank">Citibank</option>
                        <option value="diamond">Diamond Bank</option>
                        <option value="ecobank">Ecobank</option>
                        <option value="fidelity">Fidelity Bank</option>
                        <option value="fcmb">First City Monument Bank (FCMB)</option>
                        <option value="fsdh">FSDH Merchant Bank</option>
                        <option value="gtb">Guarantee Trust Bank (GTB)</option>
                        <option value="heritage">Heritage Bank</option>
                        <option value="Keystone">Keystone Bank</option>
                        <option value="rand">Rand Merchant Bank</option>
                        <option value="skye">Skye Bank</option>
                        <option value="stanbic">Stanbic IBTC Bank</option>
                        <option value="standard">Standard Chartered Bank</option>
                        <option value="sterling">Sterling Bank</option>
                        <option value="suntrust">Suntrust Bank</option>
                        <option value="union">Union Bank</option>
                        <option value="uba">United Bank for Africa (UBA)</option>
                        </select>
                    </div> 
                </div>
            </div>
            <div class="verify-reset">
            <button class="button is-primary is-rounded is-small">
                Verify
            </button>
            <button class="button is-primary is-rounded is-small">
                Reset
            </button>
            </div>
        </form>
    </main>
</template>

<script>
export default {
    head() {
        return {
            title: "AccountVerifi: Verify",
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