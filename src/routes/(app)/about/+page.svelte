
<script>
  let rows = [];
  let debtorRates = [];

  function addRow() {
    const newRowId = rows.length + 1;
    rows = [...rows, { id: newRowId, name: "", age: "", invoice: "" }];
    debtorRates = [...debtorRates, 0]; // Initialize debtor rate for the new row
  }

  function decreaseRate(index) {
    if (debtorRates[index] > 0) {
      debtorRates[index]--;
    }
  }

  function increaseRate(index) {
    if (debtorRates[index] < 10) {
      debtorRates[index]++;
    }
  }
</script>
  
  

<h1> hello </h1>



<table class="w-full bg-white border-collapse shadow-sm rounded-lg overflow-hidden">
  <thead>
    <tr>
      <th class="border p-2">ID</th>
      <th class="border p-2">Name</th>
      <th class="border p-2">Chances of timely payment</th>
      <th class="border p-2">Invoice</th>
    </tr>
  </thead>
  <tbody>
    {#each rows as row, index}
    <tr key={row.id}>
      <td class="border p-2">{row.id}</td>
      <td class="border p-2">
        <input type="text" bind:value={row.name} class="w-full px-2 py-1 rounded overflow-hidden" />
      </td>
      <td class="border p-2">
        <div class="items-center">
          <button
            type="button"
            id="minus"
            on:click={() => decreaseRate(index)}
            disabled={debtorRates[index] === 0}
            class="w-10 h-10 leading-10 text-gray-600 transition hover:opacity-75"
          >
            &minus;
          </button>

          <input
            type="number"
            disabled
            id="Quantity"
            bind:value={debtorRates[index]}
            class="h-10 w-16 rounded border-gray-200 text-center [-moz-appearance:_textfield] sm:text-sm [&::-webkit-outer-spin-button]:m-0 [&::-webkit-outer-spin-button]:appearance-none [&::-webkit-inner-spin-button]:m-0 [&::-webkit-inner-spin-button]:appearance-none"
          />

          <button
            type="button"
            id="plus"
            on:click={() => increaseRate(index)}
            disabled={debtorRates[index] === 10}
            class="w-10 h-10 leading-10 text-gray-600 transition hover:opacity-75"
          >
            &plus;
          </button>
        </div>
      </td>
      <td class="border p-2">
        <input type="file" bind:value={row.invoice} class="w-full px-2 py-1 rounded" />
      </td>
    </tr>
    {/each}
  </tbody>
</table>

<button type="button" class="mt-4 px-4 py-2 bg-blue-700 text-white rounded" on:click={addRow}>Add</button>