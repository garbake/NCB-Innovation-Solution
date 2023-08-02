<!-- component -->
<!-- <link rel="stylesheet" href="https://demos.creative-tim.com/notus-js/assets/styles/tailwind.css"> -->

<style>
    /* The glide-in transition */
    .glide-in {
      opacity: 0; /* Start with opacity 0 to make it invisible */
      transform: translateY(-20px); /* Slide up 20px */
      transition: opacity 0.8s ease, transform 0.8s ease; /* Define the transition properties */
    }
  
    /* Remove the glide-in transition after it has taken effect */
    .glide-in.active {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
  
  <script>
    // JavaScript to add the active class after the page loads
    import { onMount } from 'svelte';
  
    let isActive = false;
  
    onMount(() => {
      // Delay the addition of the active class slightly to allow the CSS transition to take effect
      setTimeout(() => {
        isActive = true;
      }, 50);
    });
  </script>

<!-- relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded-lg bg-gray-100 border-0 -->
<section class="py-1">
  <div class="w-full lg:w-6/12 px-4 mx-auto mt-6">
    <div
    class="{`relative flex flex-col min-w-0 break-words w-full mb-6 shadow-lg rounded-lg bg-gray-100 border-0 ${isActive ? 'glide-in active' : 'glide-in'}`}">
      <div class="rounded-t bg-white mb-0 px-6 py-6">
        <div class="text-center flex justify-between">
          <h6 class="text-blue-700 text-xl font-bold">Login</h6>
          <!-- <button class="bg-pink-500 text-white active:bg-pink-600 font-bold uppercase text-xs px-4 py-2 rounded shadow hover:shadow-md outline-none focus:outline-none mr-1 ease-linear transition-all duration-150" type="button">
          Settings
        </button> -->
        </div>
      </div> 
      <div class="flex-auto px-4 lg:px-10 py-10 pt-0">
        <form action="/portal">
         
          <h6 class="text-blueGray-400 text-sm mt-3 mb-6 font-bold uppercase">
            credentials information
          </h6>

          <div class="">
            <!-- Username -->
            <div class="w-full  px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  enter username
                </label>
                <input
                  type="text"
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150"
                  placeholder="username" required
                />
              </div>
            </div>
            <!--  password -->
            <div class="w-full  px-4">
              <div class="relative w-full mb-3">
                <label
                  class="block uppercase text-blueGray-600 text-xs font-bold mb-2"
                  for="grid-password"
                >
                  Enter password
                </label>
                <input
                  type="password" 
                  class="border-0 px-3 py-3 placeholder-blueGray-300 text-blueGray-600 bg-white rounded text-sm shadow focus:outline-none focus:ring w-full ease-linear transition-all duration-150 "
                  placeholder="••••••••"
                  required
                />
                
              </div>
            </div>
          </div>
          <hr class="mt-6 border-b-1 border-blue-700" />

          <div class="flex flex-wrap">

            <div class="w-full  px-4 py-4">
              <button
                type="submit"
                class="block w-full rounded-lg bg-blue-800 hover:bg-blue-700 transition px-5 py-3 text-sm font-medium text-white"
              >
                Login
              </button>

              <p class="pt-3 text-center text-sm text-gray-500">
                No account?
                <a class="  text-blue-800 hover:underline " href="/signup">Signup</a>
              </p>
            </div>
            
          </div>
        </form>
      </div>
    </div>
  </div>
</section>
