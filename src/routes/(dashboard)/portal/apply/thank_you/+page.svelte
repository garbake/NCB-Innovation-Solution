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

<div>
    <div class="flex items-center justify-center min-h-screen">
        <div class="{`flex flex-col items-center space-y-2 ${isActive ? 'glide-in active' : 'glide-in'}`}">

            

            <svg
                xmlns="http://www.w3.org/2000/svg"
                class="text-green-600 w-28 h-28"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="1"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"
                />
            </svg>
            <div class="flex flex-col items-center justify-center">
                <h1 class="text-4xl font-bold">Thank You !</h1>
                <p class="text-center">
                    Thank you for your Applying! You will be contacted via email within 24 hours.
                </p>
            </div>
            <a
                href="/portal" class="inline-flex items-center px-4 py-2 text-white bg-blue-800 border border-indigo-600 rounded rounded-full hover:bg-blue-700 focus:outline-none focus:ring"
            >
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="w-3 h-3 mr-2"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2"
                >
                    <path
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        d="M7 16l-4-4m0 0l4-4m-4 4h18"
                    />
                </svg>
                <span class="text-sm font-medium"> Home </span>
            </a>
        </div>
    </div>
</div>
