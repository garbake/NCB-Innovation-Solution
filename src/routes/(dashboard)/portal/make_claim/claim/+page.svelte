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
        Please describe to us your situation.
        </label>

        <textarea
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5"
            placeholder="Description"
            required
        />

  
            <!-- Your Step 1 form fields here -->
            <div class="pt-5">
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

                <label class="pt-4 block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-state">
                    Please Upload The Invoice Overdue 
                </label>
                <div class="pt-5">
                <div  class=" pl-50 pr-50 flex items-center justify-center w-full">
                    <label for="dropzone-file" class="flex flex-col items-center justify-center w-full h-64 border-2 border-gray-300 border-dashed rounded-lg cursor-pointer bg-gray-50 hover:bg-gray-100 ">
                        <div class="flex flex-col items-center justify-center pt-5 pb-6">
                            <svg class="w-8 h-8 mb-4 text-gray-500 dark:text-gray-400" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 16">
                                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 13h3a3 3 0 0 0 0-6h-.025A5.56 5.56 0 0 0 16 6.5 5.5 5.5 0 0 0 5.207 5.021C5.137 5.017 5.071 5 5 5a4 4 0 0 0 0 8h2.167M10 15V6m0 0L8 8m2-2 2 2"/>
                            </svg>
                            <p class="mb-2 text-sm text-gray-500 dark:text-gray-400"><span class="font-semibold">Click to upload</span> or drag and drop</p>
                            <p class="text-xs text-gray-500 dark:text-gray-400">SVG, PNG, JPG or GIF </p>
                        </div>
                        <input id="dropzone-file" type="file" class="hidden" />
                    </label>
                    </div>

                    <label class="pt-4 block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2" for="grid-state">
                        Please upload your attempts of retrieving payment. I.e. Email, call logs

                    </label>
                    <div class="pt-5">
                    <div  class=" pl-50 pr-50 flex items-center justify-center w-full">
                        <label for="dropzone-file" class="flex flex-col items-center justify-center w-full h-64 border-2 border-gray-300 border-dashed rounded-lg cursor-pointer bg-gray-50 dark:hover:bg-bray-800 dark:bg-gray-700 hover:bg-gray-100">
                            <div class="flex flex-col items-center justify-center pt-5 pb-6">
                                <svg class="w-8 h-8 mb-4 text-gray-500 dark:text-gray-400" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 20 16">
                                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 13h3a3 3 0 0 0 0-6h-.025A5.56 5.56 0 0 0 16 6.5 5.5 5.5 0 0 0 5.207 5.021C5.137 5.017 5.071 5 5 5a4 4 0 0 0 0 8h2.167M10 15V6m0 0L8 8m2-2 2 2"/>
                                </svg>
                                <p class="mb-2 text-sm text-gray-500 dark:text-gray-400"><span class="font-semibold">Click to upload</span> or drag and drop</p>
                                <p class="text-xs text-gray-500 dark:text-gray-400">SVG, PNG, JPG or GIF </p>
                            </div>
                            <input id="dropzone-file" type="file" class="hidden" />
                        </label>
                        </div>


            
        </div>
    </div>
    <button
            type="submit"
            class="mt-6 px-4 py-2 mb-3 ml-3 bg-blue-600 text-white rounded-lg focus:outline-none focus:ring focus:border-blue-300"
        >
            Submit
        </button>
</form>

