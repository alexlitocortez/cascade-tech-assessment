<template>
  <section>
    <div>
      <h1>Statement</h1>
    </div>
    <div
      class="flex-one"
      v-for="statement in statements"
      in
      statement.transactions
      :key="statement"
    >
      <div class="card">
        <h1>Successful Transaction #1</h1>
        <p>Account Number: {{ statement.Transactions[0].AccountNumber }}</p>
        <p>
          Transaction Type: {{ statement.Transactions[0].TransactionTypeId }}
        </p>
        <p>Transaction Date: {{ statement.Transactions[0].TransactionDate }}</p>
        <p>Amount: {{ statement.Transactions[0].Amount }}</p>
        <p>Description: {{ statement.Transactions[0].Description }}</p>
        <p>Billed?: {{ statement.Transactions[0].Billed }}</p>
        <p>Merchant Name: {{ statement.Transactions[0].MerchantName }}</p>
        <p>Merchant ID: {{ statement.Transactions[0].MerchantId }}</p>
      </div>
      <div class="card">
        <h1>Unsettled Transaction #1</h1>
        <p>Account Number: {{ statement.NotSettled[0].AccountNumber }}</p>
        <p>Transaction Type: {{ statement.NotSettled[0].TransactionTypeId }}</p>
        <p>Transaction Date: {{ statement.NotSettled[0].TransactionDate }}</p>
        <p>Amount: {{ statement.NotSettled[0].Amount }}</p>
        <p>Description: {{ statement.NotSettled[0].Description }}</p>
        <p>Merchant Name: {{ statement.NotSettled[0].MerchantName }}</p>
        <p>Merchant ID: {{ statement.NotSettled[0].MerchantId }}</p>
      </div>
      <div class="card">
        <h1>Successful Transaction #2</h1>
        <p>Account Number: {{ statement.Transactions[1].AccountNumber }}</p>
        <p>
          Transaction Type: {{ statement.Transactions[1].TransactionTypeId }}
        </p>
        <p>Transaction Date: {{ statement.Transactions[1].TransactionDate }}</p>
        <p>Amount: {{ statement.Transactions[1].Amount }}</p>
        <p>Description: {{ statement.Transactions[1].Description }}</p>
        <p>Billed?: {{ statement.Transactions[1].Billed }}</p>
        <p>Merchant Name: {{ statement.Transactions[1].MerchantName }}</p>
        <p>Merchant ID: {{ statement.Transactions[1].MerchantId }}</p>
      </div>
    </div>
    <div class="flex-two" v-for="statement in statements" :key="statement">
      <div class="card">
        <h1>Unsettled Transaction #2</h1>
        <p>Account Number: {{ statement.NotSettled[1].AccountNumber }}</p>
        <p>Transaction Type: {{ statement.NotSettled[1].TransactionTypeId }}</p>
        <p>Transaction Date: {{ statement.NotSettled[1].TransactionDate }}</p>
        <p>Amount: {{ statement.NotSettled[1].Amount }}</p>
        <p>Description: {{ statement.NotSettled[1].Description }}</p>
        <p>Billed?: {{ statement.NotSettled[1].Billed }}</p>
        <p>Merchant Name: {{ statement.NotSettled[1].MerchantName }}</p>
        <p>Merchant ID: {{ statement.NotSettled[1].MerchantId }}</p>
      </div>
      <div class="card">
        <h1>Successful Transaction #3</h1>
        <p>Account Number: {{ statement.Transactions[2].AccountNumber }}</p>
        <p>
          Transaction Type: {{ statement.Transactions[2].TransactionTypeId }}
        </p>
        <p>Transaction Date: {{ statement.Transactions[2].TransactionDate }}</p>
        <p>Amount: {{ statement.Transactions[2].Amount }}</p>
        <p>Description: {{ statement.Transactions[2].Description }}</p>
        <p>Billed?: {{ statement.Transactions[2].Billed }}</p>
        <p>Merchant Name: {{ statement.Transactions[2].MerchantName }}</p>
        <p>Merchant ID: {{ statement.Transactions[2].MerchantId }}</p>
      </div>
    </div>
    <section>
      <h1>Available Balance Minus Successful Transactions</h1>
      <p>250.1</p>
    </section>
    <section>
      <h1>Available Balance Minus Unsettled and Successful Transactions</h1>
      <p>108.28</p>
    </section>
  </section>
</template>

<script>
// Importing array from our JSON file

import json from "../assets/statement.json";

export default {
  data: function () {
    return {
      statements: json,
    };
  },
  mounted: function () {
    console.log(json);
  },
};
</script>

<style>
.flex-one,
.flex-two {
  display: flex;
  justify-content: space-around;
  margin-top: 3rem;
}

h1 {
  text-align: center;
}

.card {
  width: 25rem;
  height: 25rem;
  box-shadow: 2px 1px 1px 1px black;
  text-align: left;
}

@media (max-width: 1250px) {
  .flex-one,
  .flex-two {
    flex-direction: column;
    margin: auto;
    justify-content: center;
    align-items: center;
  }
}
</style>
