<!-- component -->
<!-- <link rel="stylesheet" href="https://demos.creative-tim.com/notus-js/assets/styles/tailwind.css"> -->

<script>
  let rows = [];
  let debtorRate = 0;

  function addRow() {
    const newRowId = rows.length + 1;
    rows = [...rows, { id: newRowId, name: "", age: "", invoice: "" }];
  }

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

<svelte:head>
  <script
    src="https://cdnjs.cloudflare.com/ajax/libs/flowbite/1.7.0/datepicker.min.js"
  ></script>
</svelte:head>

<section class=" py-1">
  <div class="w-full lg:w-8/12 px-4 mx-auto mt-6">
    <div
      class="relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded-lg bg-gray-100 border-0"
    >
      <div class="rounded-t bg-white mb-0 px-6 py-6">
        <div class="text-center flex justify-between">
          <h6 class="text-blue-700 text-xl font-bold">My account</h6>
          <!-- <button class="bg-pink-500 text-white active:bg-pink-600 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 ease-linear transition-all duration-150" type="button">
          Settings
        </button> -->
        </div>
      </div>
      <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
        <form>
          <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase">
            User Information
          </h6>

          <div class="flex flex-wrap">
            <!-- first name -->
            <div class="w-full lg:w-4/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  first name
                </label>
                <input
                  type="email"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  placeholder="Jane"
                />
              </div>
            </div>
            <!-- last name -->
            <div class="w-full lg:w-4/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  last name
                </label>
                <input
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  placeholder="Doe"
                />
              </div>
            </div>
            <!-- gender -->
            <div class="w-full lg:w-4/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="gender"
                >
                  Gender
                </label>
                <select
                  id="gender"
                  name="gender"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                >
                  <option value="" disabled selected>Select your gender</option>
                  <option value="male">Male</option>
                  <option value="female">Female</option>
                </select>
              </div>
            </div>

            <!-- username -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  Username
                </label>
                <input
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  placeholder="JaneDoe"
                />
              </div>
            </div>
            <!-- Email Address -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  Email address
                </label>
                <input
                  type="email"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  placeholder="janed@gmail.com"
                />
              </div>
            </div>

            <!-- DOB -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  date of birth
                </label>
                <input
                  type="date"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value="Lucky"
                />
              </div>
            </div>

            <!-- Telephone -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  Telephone
                </label>
                <input
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value="+1 (876)"
                />
              </div>
            </div>
          </div>

          <hr class="mt-6 border-b-1 border-blueGray-300" />

          <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase">
            Business Information
          </h6>
          <div class="flex flex-wrap">
            <!-- BUsiness Name -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  Business Name
                </label>
                <input
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  placeholder="Doe's Enterprise"
                />
              </div>
            </div>
            <!-- Business registry Number -->
            <div class="w-full lg:w-6/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  Business Registration Number
                </label>
                <input
                  type="number"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  placeholder="345524443"
                />
              </div>
            </div>

            <!-- Address -->
            <div class="w-full lg:w-12/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  Address
                </label>
                <input
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  Placeholder="21 Red Hills Rd, Kingston 20, Shop 12"
                />
              </div>
            </div>

            <div class="w-full lg:w-4/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  City
                </label>
                <input
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value="New York"
                />
              </div>
            </div>

            <div class="w-full lg:w-4/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  Country
                </label>
                <input
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value="United States"
                />
              </div>
            </div>

            <div class="w-full lg:w-4/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  Postal Code
                </label>
                <input
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  value="Postal Code"
                />
              </div>
            </div>
          </div>

          <hr class="mt-6 border-b-1 border-blue-800" />

          <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase">
            debtors information
          </h6>
          <div class="flex flex-wrap">
            <div class="w-full lg:w-12/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  About Debtor
                </label>
                <table
                  class="w-full bg-white border-collapse shadow-sm rounded-lg overflow-hidden"
                >
                  <thead>
                    <tr>
                      <th class="border p-2">ID</th>
                      <th class="border p-2">Name</th>
                      <th class="border p-2">Chances of timely payment</th>
                      <th class="border p-2">Invoice</th>
                    </tr>
                  </thead>
                  <tbody>
                    {#each rows as row}
                      <tr key={row.id}>
                        <td class="border p-2">{row.id}</td>
                        <td class="border p-2">
                          <input
                            type="text"
                            bind:value={row.name}
                            class="w-full px-2 py-1 rounded overflow-hidden"
                          />
                        </td
                        >
                        <td class="border p-2">
                          <div class="items-center">
                            <button
                              type="button"
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
                              type="button"
                              on:click={increaseRate}
                              disabled={debtorRate === 10}
                              class="w-10 h-10 leading-10 text-gray-600 transition hover:opacity-75"
                            >
                              &plus;
                            </button>
                          </div>
                        </td>
                        <td class="border p-2">
                          <input
                            type="file"
                            bind:value={row.invoice}
                            class="w-full px-2 py-1 rounded"
                          />
                        </td>
                      </tr>
                    {/each}
                  </tbody>
                </table>

                <button
                  type="button"
                  class="mt-4 px-4 py-2 bg-blue-700 text-white rounded"
                  on:click={addRow}>Add</button
                >
              </div>
            </div>
          </div>
          <hr class="mt-6 border-b-1 border-blue-700" />

          <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase">
            About Me
          </h6>
          <div class="flex flex-wrap">
            <div class="w-full lg:w-12/12 px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  About Business
                </label>
                <textarea
                  typeof="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  rows="4"
                >
                  A beautiful UI Kit and Admin for JavaScript &amp; Tailwind
                  CSS. It is Freeand Open Source.</textarea
                >
              </div>
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</section>
