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

<section
    class="relative bg-[url(https://images.unsplash.com/photo-1450101499163-c8848c66ca85?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80)] bg-cover bg-center bg-no-repeat"
>
    <div
        class="absolute inset-0 bg-white/75 bg-transparent from-white/95 to-white/25 ltr:bg-gradient-to-r rtl:bg-gradient-to-l"
    />

    <div
        class="relative mx-auto max-w-screen-xl px-4 py-32 sm:px-6 lg:flex lg:h-screen lg:items-center lg:px-8 flex items-center justify-center"
    >
        <div class="{`max-w-xl text-center ltr:sm:text-left rtl:sm:text-right ${isActive ? 'glide-in active' : 'glide-in'}`}">
            <h1 class="text-3xl text-blue-800 font-extrabold sm:text-5xl">
                Welcome to NCB'S Trade Credit

                <strong class="block font-extrabold text-yellow-400">
                    Insurance Management System
                </strong>
            </h1>

            <p class="mt-4 max-w-lg sm:text-xl/relaxed">
                <!-- Fill here-->
            </p>

            <div
                class="mt-8 flex flex-wrap gap-4 text-center items-center justify-center"
            >
                <a
                    href="#"
                    class="block w-full rounded bg-blue-800 px-12 py-3 text-sm font-medium text-white shadow hover:bg-rose-700 focus:outline-none focus:ring active:bg-rose-500 sm:w-auto"
                >
                    Apply Now
                </a>
            </div>
        </div>
    </div>
</section>
