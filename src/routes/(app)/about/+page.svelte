
  
  
  

<h1> hello </h1>

<script>
  let debtorRate = 0;

  function decreaseRate() {
    if (debtorRate > 0) {
      debtorRate--;
    }
  }

  function increaseRate() {
    if (debtorRate < 10) {
      debtorRate++;
    }
  }
</script>

<div>
  <label for="Quantity" class="sr-only">Quantity</label>

  <div class="flex items-center gap-1">
    <button
      on:click={decreaseRate}
      disabled={debtorRate === 0}
      class="w-10 h-10 leading-10 text-gray-600 transition hover:opacity-75"
    >
      &minus;
    </button>

    <input
      type="number"
      id="Quantity"
      bind:value={debtorRate}
      class="h-10 w-16 rounded border-gray-200 text-center [-moz-appearance:_textfield] sm:text-sm [&::-webkit-outer-spin-button]:m-0 [&::-webkit-outer-spin-button]:appearance-none [&::-webkit-inner-spin-button]:m-0 [&::-webkit-inner-spin-button]:appearance-none"
    />

    <button
      on:click={increaseRate}
      disabled={debtorRate === 10}
      class="w-10 h-10 leading-10 text-gray-600 transition hover:opacity-75"
    >
      &plus;
    </button>
  </div>
</div>
