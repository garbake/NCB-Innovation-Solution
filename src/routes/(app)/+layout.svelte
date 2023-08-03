<script lang="ts">
    import ncblogo from "$lib/images/ncb-logo1.png"
</script>

<header class="bg-white">
    <div class="mx-auto max-w-screen-xl px-4 sm:px-6 lg:px-8">
      <div class="flex h-16 items-center justify-between">
        <div class="md:flex md:items-center md:gap-12">
          <a class="block" href="/">
            <span class="sr-only">Home</span>
            <img class=" h-30 w-44  object-cover" src={ncblogo} />
          </a>
        </div>
  
        <div class="hidden md:block">
          <nav aria-label="Global">
            <ul class="flex items-center gap-6 text-lg text-">
              <li>
                <a
                  class="text-blue-800 transition hover:text-blue-700"
                  href="/"
                >
                  Home
                </a>
              </li>
  
              <li>
                <a
                class="text-blue-800 transition hover:text-blue-700"
                  href="/about"
                >
                  About
                </a>
              </li>
  
              <li>
                <a
                class="text-blue-800 transition hover:text-blue-700"
                  href="#"
                >
                  Contact Us
                </a>
              </li>
  
              <li>
                <a
                  class="text-blue-800 transition hover:text-blue-700"
                  href="#"
                >
                  Who Are We?
                </a>
              </li>
  
              <li>
                <a
                  class="text-blue-800 transition hover:text-blue-700"
                  href="#"
                >
                  What We Do
                </a>
              </li>
  
              <li>
                <a
                class="text-blue-800 transition hover:text-blue-700"
                  href="/portal"
                >
                  TCIMS Portal
                </a>
              </li>
            </ul>
          </nav>
        </div>
  
        <div class="flex items-center gap-4">
          <div class="sm:flex sm:gap-4">
            <a
              class="rounded-md bg-blue-800 hover:bg-blue-700 transition px-5 py-2.5 text-sm font-medium text-white shadow"
              href="/login"
            >
            Customer Login  
            </a>

            <a
              class="rounded-md bg-blue-800 hover:bg-blue-700 transition px-5 py-2.5 text-sm font-medium text-white shadow"
              href="/employee_portal/"
            >
            Employeee Login
            </a>

            <div class="hidden sm:flex">
              <a
                class="rounded-md bg-gray-100  hover:bg-blue-800 transition hover:text-white  px-5 py-2.5 text-sm font-medium text-blue-800"
                href="/signup"
              >
                Signup
              </a>
            </div>
            
          </div>
          
  
          <div class="block md:hidden">
            <button
              class="rounded bg-gray-100 p-2 text-gray-600 transition hover:text-gray-600/75"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M4 6h16M4 12h16M4 18h16"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>
    </div>
  </header>

<slot/>


<footer class="bg-blue-900">
    <div class=" max-w-screen-xl px-4 pb-6  sm:px-6 lg:px-8">
      
  
      <div
        class="mt-16 grid grid-cols-1 gap-8 border-t border-gray-100 pt-16 md:grid-cols-4 lg:grid-cols-6"
      >
        <div class="text-center sm:text-left">
          <p class="text-lg font-medium text-white">CONTACT US</p>
  
          <ul class="mt-8 space-y-4 text-sm">
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Company History
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Meet the Team
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Employee Handbook
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Careers
              </a>
            </li>
          </ul>
        </div>
  
        <div class="text-center sm:text-left">
          <p class="text-lg font-medium text-white">CUSTOMER SERVICES</p>
  
          <ul class="mt-8 space-y-4 text-sm">
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Web Development
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Web Design
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Marketing
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Google Ads
              </a>
            </li>
          </ul>
        </div>
  
        <div class="text-center sm:text-left">
          <p class="text-lg font-medium text-white">INFORMATION</p>
  
          <ul class="mt-8 space-y-4 text-sm">
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Online Guides
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Conference Notes
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Forum
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Downloads
              </a>
            </li>
  
            <li>
              <a class="text-white transition hover:text-gray-700/75" href="/">
                Upcoming Events
              </a>
            </li>
          </ul>
        </div>
  
        <div class="text-center sm:text-left md:col-span-4 lg:col-span-2">
          
  
          <div class="mx-auto mt-8 max-w-md sm:ms-0 ">
            <p
              class="text-center leading-relaxed text-white ltr:sm:text-left rtl:sm:text-right"
            >
            Copyright  &copy; 1999-2023 NCB Jamaica
            </p>
  
          </div>
        </div>
      </div>      
    </div>
  </footer>