<form action="https://www.jncb.com/Business/Banking/Online-Banking">
    <div class="pt-5 pl-5 w-full px-3 mb-6 md:mb-0">
        <div class="mx-auto max-w-lg text-center">
            <h2 class="text-2xl font-bold text-blue-900 md:text-3xl">
                 TCI Claim Form
            </h2>

            <p
                class="block font-extrabold uppercase tracking-wide text-gray-700 text-xs mb-2 mt-2"
            >
                We Will Require Somemore Information About This Claim
            </p>
        </div>

        <label
            class="pt-4 block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-state"
        >
            Please Enter Some Detials about the Non-payment 
        </label>

        <textarea
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
            placeholder="Description"
            required
        />

        <div class="grid gap-6 mb-6 md:grid-cols-2 px-3 pt-3">
            <!-- Your Step 1 form fields here -->
            <div>
                <label
                    for="type_of_business"
                    class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
                    >When was this invoice payment due?</label
                >
                <input
                    type="date"
                    id="first_name"
                    class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
                    placeholder="John"
                    required
                />
            </div>

            
        </div>
    </div>
</form>
