<script lang="ts">
  let amount = "0";

  function applyFormatting() {
    amount = new Intl.NumberFormat("nl-NL", {
      style: "currency",
      currency: "EUR",
    }).format(Number(amount));
  }
</script>

<div class="wizard">
  <h2>Welk bedrag staat er op dit moment open?</h2>
  <input
    bind:value={amount}
    on:blur={applyFormatting}
    type="text"
    name="currency-field"
    id="currency-field"
    data-type="currency"
    placeholder="€50.000,00"
  />
</div>

<style>
  .wizard {
    display: flex;
    flex-direction: column;
  }

  input {
    border: 2px solid #333;
    border-radius: 5px;
    color: #333;
    font-size: 32px;
    margin: 0 0 20px;
    padding: 0.5rem 1rem;
    width: 100%;
  }
</style>
