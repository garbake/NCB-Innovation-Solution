<script>
    import ncblogo from "$lib/images/ncb_logo.png"
</script>

<form action="https://www.jncb.com/Business/Banking/Online-Banking">
    <div class="mx-auto max-w-lg text-center py-4 px-4">
        <h2 class="text-2xl font-bold text-blue-900 md:text-3xl">
            Payment Info
        </h2>

        <p class="text-gray-500 sm:mt-2 sm:block">Make secure payments</p>
    </div>

    <div class="pl-20 pr-20">
        <div class=" pt-4 pb-4 flex grid-cols-1 gap-3">
            <div class="pt-2">
                <h1 class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2">Express Payment: </h1>
            </div>

            <div>
                <button
                    type="submit"
                    class="flex items-center justify-center w-full rounded-lg bg-blue-800 hover:bg-blue-700 transition px-5 py-3 text-sm font-medium text-white"
                >
                    <img src="{ncblogo}" class=" w-11 mr-2" alt="NCB Logo">
                    Make Payment via Existing NCB Amount
                </button>
            </div>
        </div>

        <div class=" flex flex-wrap -mx-3 mb-6">
            <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
                <label
                    class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
                    for="grid-first-name"
                >
                    First Name
                </label>
                <input
                    class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
                    id="grid-first-name"
                    type="text"
                    placeholder="Jane"
                />
            </div>
            <div class="w-full md:w-1/2 px-3">
                <label
                    class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
                    for="grid-last-name"
                >
                    Last Name
                </label>
                <input
                    class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
                    id="grid-last-name"
                    type="text"
                    placeholder="Doe"
                />
            </div>
        </div>
        <div class="flex flex-wrap -mx-3 mb-6">
            <div class="w-full px-3">
                <label
                    class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
                    for="grid-last-name"
                >
                    Credit Card Number
                </label>
                <input
                    class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
                    id="grid-last-name"
                    type="text"
                    placeholder="Doe"
                />
            </div>
        </div>
        <div class="flex flex-wrap -mx-3 mb-2">
            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                <label
                    class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
                    for="grid-city"
                >
                    CVV Security Code
                </label>
                <input
                    class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
                    id="grid-city"
                    type="text"
                    placeholder="123"
                />
            </div>
            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                <label
                    class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
                    for="grid-state"
                >
                    Expiration Month
                </label>
                <div class="relative">
                    <select
                        class="block appearance-none w-full bg-gray-200 border border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
                        id="grid-state"
                    >
                        <option value="">Month</option>
                        <option value="01">January</option>
                        <option value="02">February</option>
                        <option value="03">March</option>
                        <option value="04">April</option>
                        <option value="05">May</option>
                        <option value="06">June</option>
                        <option value="07">July</option>
                        <option value="08">August</option>
                        <option value="09">September</option>
                        <option value="10">October</option>
                        <option value="11">November</option>
                        <option value="12">December</option>
                    </select>
                    <div
                        class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700"
                    >
                        <svg
                            class="fill-current h-4 w-4"
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 20 20"
                            ><path
                                d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                            /></svg
                        >
                    </div>
                </div>
            </div>

            <div class="w-full md:w-1/3 px-3 mb-6 md:mb-0">
                <label
                    class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
                    for="grid-state"
                >
                    Expiration Year
                </label>
                <div class="relative">
                    <select
                        class="block appearance-none w-full bg-gray-200 border border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
                        id="grid-state"
                    >
                        <option value="23">2023</option>
                        <option value="24">2024</option>
                        <option value="25">2025</option>
                        <option value="26">2026</option>
                        <option value="27">2027</option>
                        <option value="28">2028</option>
                    </select>
                    <div
                        class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700"
                    >
                        <svg
                            class="fill-current h-4 w-4"
                            xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 20 20"
                            ><path
                                d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                            /></svg
                        >
                    </div>
                </div>
            </div>
        </div>
        <div class="px-2">
            <div class="flex justify-center items-center pt-4">
                <h2
                    class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
                >
                    Payment Methods:
                </h2>
                <img
                    src="https://leadershipmemphis.org/wp-content/uploads/2020/08/780370.png"
                    class="h-8 ml-3"
                />
            </div>
        </div>
        <div class="flex flex-wrap">
            <div class="w-full px-4 py-4">
                <button
                    type="submit"
                    class="block w-full rounded-lg bg-blue-800 hover:bg-blue-700 transition px-5 py-3 text-sm font-medium text-white"
                >
                    Make Payment
                </button>
            </div>
        </div>
    </div>
</form>
