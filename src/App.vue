<template>
  <div>
    <StatementTransactions></StatementTransactions>
  </div>
</template>

<script>
import StatementTransactions from "./components/StatementTransactions";

export default {
  components: {
    StatementTransactions,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 1rem;
  max-width: 960px;
  margin: 0 auto;
}

p,
h3 {
  grid-column: span 3;
}

.list-group {
  border: 3px solid;
  border-radius: 0.5rem;
  padding: 1rem;
  margin-bottom: 1rem;
}

.list-group:first-child {
  font-weight: bold;
  font-size: 2.5rem;
  margin: 1rem 0;
}

.list-group p:last-child {
  font-style: italic;
  font-size: 0.8rem;
}
</style>
