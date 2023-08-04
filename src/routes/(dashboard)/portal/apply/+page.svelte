<script>
    import { createEventDispatcher } from "svelte";
    


	let showModal = false;
    const dispatch = createEventDispatcher();
    let currentStep = 1;
    let debtorRates = 0;

    // @ts-ignore
    function goToStep(step) {
        currentStep = step;
    }

    function nextStep() {
        if (currentStep < 3) {
            currentStep++;
        }
    }

    // @ts-ignore
    function previousStep() {
        if (currentStep > 1) {
            currentStep--;
        }
    }

    function handleSubmit() {
        // Handle form submission here
        dispatch("formSubmitted");
    }

    function decreaseRate() {
    if (debtorRates > 0) {
      debtorRates--;
    }
  }

  function increaseRate() {
    if (debtorRates < 10) {
      debtorRates++;
    }
  }

</script>


  

<ol
    class="flex items-center justify-center w-full p-3 space-x-2 text-sm font-medium text-center text-gray-500 bg-white border border-gray-200 rounded-lg shadow-sm dark:text-gray-400 sm:text-base  sm:p-4 sm:space-x-4"
>
    {#each [1, 2, 3] as step}
        <li
            class="flex items-center cursor-pointer {currentStep === step
                ? 'text-blue-600 dark:text-blue-500'
                : 'text-gray-500'}"
            on:click={() => goToStep(step)}
        >
            <span
                class="flex items-center justify-center w-5 h-5 mr-2 text-xs border {currentStep ===
                step
                    ? 'border-blue-600 dark:border-blue-500'
                    : 'border-gray-500'} rounded-full shrink-0 dark:border-gray-400"
            >
                {step}
            </span>
            {#if step === 1}
                Business <span class="hidden sm:inline-flex sm:ml-2">Info</span>
            {:else if step === 2}
                Debtors <span class="hidden sm:inline-flex sm:ml-2">Info</span>
            {:else}
                Review
            {/if}
            {#if currentStep !== step}
                <svg
                    class="w-3 h-3 ml-2 sm:ml-4"
                    aria-hidden="true"
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 12 10"
                >
                    <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="m7 9 4-4-4-4M1 9l4-4-4-4"
                    />
                </svg>
            {/if}
        </li>
    {/each}
</ol>

{#if currentStep === 1}
    <form on:submit|preventDefault={nextStep}>
        <div class="grid gap-6 mb-6 md:grid-cols-2 px-3 pt-3">
            <!-- Your Step 1 form fields here -->
            <div>
                <label
                    for="type_of_business"
                    class="block mb-2 text-sm font-medium text-gray-900"
                    >Type of business</label
                >
                <select
                    id="first_name"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
                    placeholder="John"
                    required
                >
                    <option value="" disabled selected
                        >Select your business type</option
                    >
                    <option value="retailer">Retailer</option>
                </select>
            </div>

            <div>
                <label
                    for="how-often-credit-goods"
                    class="block mb-2 text-sm font-medium text-gray-900"
                    >How often you credit goods/services</label
                >
                <select
                    id="how-often-credit-goods"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
                    placeholder=""
                    required
                >
                    <option value="" disabled selected>Select How often</option>
                    <option value="Once a several times a month">Often</option>
                    <option value="Every two weeks">Few Times a Year</option>
                    <option value="Once a year">Rearly</option>
                </select>
            </div>
        </div>

        <div class="px-3">
            <div class="mb-6">
                <label
                    for="email"
                    class="block mb-2 text-sm font-medium text-gray-900 "
                    >Describe the types of goods/services you credit</label
                >
                <textarea
                    id="email"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 "
                    placeholder="description"
                    required
                />
            </div>
            </div>


        <button
            type="submit"
            class="mt-6 px-4 py-2 mb-3 ml-3 bg-blue-600 text-white rounded-lg focus:outline-none focus:ring focus:border-blue-300"
        >
            Continue
        </button>
    </form>
{/if}

{#if currentStep === 2}
    <form on:submit|preventDefault={nextStep}>
        <div class="grid gap-6 mb-6 md:grid-cols-2 px-3 pt-3">
            <!-- Your Step 2 form fields here -->
            <div>
                <label
                    for="first_name"
                    class="block mb-2 text-sm font-medium text-gray-900 "
                    >Business name</label
                >
                <input
                    type="text"
                    id="first_name"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 "
                    placeholder="John"
                    required
                />
            </div>
            <!-- Business relationship length -->
            <div>
                <label
                    for="relationship_length"
                    class="block mb-2 text-sm font-medium text-gray-900"
                    >Business relation since</label
                >
                <input
                    type="date"
                    id="relationship_lenght"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-800 block w-full p-2.5"
                    placeholder="Doe"
                    required
                />
            </div>
            <!-- Email -->
            <div>
                <label
                    for="email"
                    class="block mb-2 text-sm font-medium text-gray-900 "
                    >Email address</label
                >
                <input
                    type="email"
                    id="email"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-800 focus:border-blue-500 block w-full p-2.5 "
                    placeholder="janenterprise@gmail.com"
                    required
                />
            </div>
            <!-- Phone number -->
            <div>
                <label
                    for="phone"
                    class="block mb-2 text-sm font-medium text-gray-900 "
                    >Phone number</label
                >
                <input
                    type="number"
                    id="phone"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 "
                    placeholder="123-45-678"
                    required
                />
            </div>
            
        </div>
        <div class="px-3">
            <div class="mb-6">
                <label
                    for="debtor_address"
                    class="block mb-2 text-sm font-medium text-gray-900 "
                >
                    Address</label
                >
                <input
                    type="text"
                    id="debtor_address"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 "
                    placeholder="up down round town"
                    required
                />
            </div>
        </div>

        <div class="grid gap-6 mb-6 md:grid-cols-2 px-3 pt-3">
             <div>
              <label for="website" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">How long haave this business Existed?</label>
              <input type="date" id="website" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5" placeholder="flowbite.com" required>
          </div>

          <div>
              <label for="visitors" class="block mb-2 text-sm font-medium text-gray-900 "> Rate their likelihood of making a timely payment, with 1 being the lowest and 10 the highest.</label>
              <button
            type="button"
            id="minus"
            on:click={() => decreaseRate()}
            disabled={debtorRates === 0}
            class="w-10 h-10 leading-10 text-gray-600 transition hover:opacity-75"
          >
            &minus;
          </button>

          <input
            type="number"
            disabled
            id="Quantity"
            bind:value={debtorRates}
            class="h-10 w-16 rounded border-gray-200 text-center [-moz-appearance:_textfield] sm:text-sm [&::-webkit-outer-spin-button]:m-0 [&::-webkit-outer-spin-button]:appearance-none [&::-webkit-inner-spin-button]:m-0 [&::-webkit-inner-spin-button]:appearance-none"
          />

          <button
            type="button"
            id="plus"
            on:click={() => increaseRate()}
            disabled={debtorRates === 10}
            class="w-10 h-10 leading-10 text-gray-600 transition hover:opacity-75"
          >
            &plus;
          </button>
          </div>

            <div>
                <label
                    for="website"
                    class="block mb-2 text-sm font-medium text-gray-900 "
                    >Have you ever credited this business before? If yes, upload
                    the last invoice</label
                >
                <input
                    type="file"
                    id="website"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 "
                    placeholder="flowbite.com"
                    required
                />
            </div>
            <div>
                <label
                    for="visitors"
                    class="block mb-2 text-sm font-medium text-gray-900"
                    >Upload current invoice</label
                >
                <input
                    type="file"
                    id="visitors"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 "
                    placeholder=""
                    required
                />
            </div>
        </div>

        <button
            type="submit"
            class="mt-6 px-4 py-2 mb-3 ml-3 bg-blue-600 text-white rounded-lg focus:outline-none focus:ring focus:border-blue-300"
        >
            Continue
        </button>
    </form>
{/if}

{#if currentStep === 3}
    <form on:submit|preventDefault={handleSubmit}>
        <div class="mb-6">
            <div class="pl-10 pr-10">
            <p class="text-xl  mb-4">By utilizing our trade credit insurance services, you hereby agree that all information provided to our company must be accurate, complete, and truthful to the best of your knowledge. Any intentional or inadvertent misrepresentation, falsification, or fraudulent activity in the information provided will not be tolerated. In the event that fraudulent activity is detected, our company reserves the right to take legal action and prosecute offenders to the fullest extent of the law. Moreover, offenders may be subject to fines and penalties as deemed appropriate by the relevant authorities. By accessing and using our trade credit insurance services, you acknowledge and consent to these terms and agree to comply with all applicable laws and regulations governing trade credit insurance.</p>
            <!-- Step 3 form fields -->
            <div>
                <!-- Your Step 3 form fields here -->
            </div>
            <button
                type="submit"
                class="mt-6 px-4 py-2 bg-blue-600 text-white rounded-lg focus:outline-none focus:ring focus:border-blue-300"
            >
                Click To Agree
            </button>
        </div>
        </div>
    </form>
{/if}
