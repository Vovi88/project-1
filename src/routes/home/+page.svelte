<!--
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
    ],
  }
  ```
-->
<nav class="bg-gray-800">
    <div class="mx-auto max-w-7xl px-2 sm:px-4 lg:px-8">
      <div class="relative flex h-16 items-center justify-between">
        <div class="flex items-center px-2 lg:px-0">
            <a href= "../">
          <div class="flex-shrink-0">
            <img class="h-8 w-auto" src="/images/UniFrame-full.svg" alt="Your Company">
          </div>
        </a>
          <div class="hidden lg:ml-6 lg:block">
            <div class="flex space-x-4">
              <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
              <a href="#" class="rounded-md bg-gray-900 px-3 py-2 text-sm font-medium text-white">Home</a>
              <a href="#" class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Explore</a>
              <a href="#" class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Universities</a>
              
            </div>
          </div>
        </div>
         <a href="#" class="ml-6 inline-flex items-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Upload</a>
        <div class="flex flex-1 justify-center px-2 lg:ml-6 lg:justify-end">
          <div class="w-full max-w-lg lg:max-w-xs">
            <label for="search" class="sr-only">Search</label>
            <div class="relative">
              <div class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-3">
                <svg class="h-5 w-5 text-gray-400" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                  <path fill-rule="evenodd" d="M9 3.5a5.5 5.5 0 100 11 5.5 5.5 0 000-11zM2 9a7 7 0 1112.452 4.391l3.328 3.329a.75.75 0 11-1.06 1.06l-3.329-3.328A7 7 0 012 9z" clip-rule="evenodd" />
                </svg>
              </div>
              <input id="search" name="search" class="block w-full rounded-md border-0 bg-gray-700 py-1.5 pl-10 pr-3 text-gray-300 placeholder:text-gray-400 focus:bg-white focus:text-gray-900 focus:ring-0 sm:text-sm sm:leading-6" placeholder="Search" type="search">
            </div>
          </div>
        </div>
        <div class="flex lg:hidden">
          <!-- Mobile menu button -->
          <button type="button" class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white" aria-controls="mobile-menu" aria-expanded="false">
            <span class="absolute -inset-0.5"></span>
            <span class="sr-only">Open main menu</span>
            <!--
              Icon when menu is closed.
  
              Menu open: "hidden", Menu closed: "block"
            -->
            <svg class="block h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
            <!--
              Icon when menu is open.
  
              Menu open: "block", Menu closed: "hidden"
            -->
            <svg class="hidden h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
        <div class="hidden lg:ml-4 lg:block">
          <div class="flex items-center">
            <button type="button" class="relative flex-shrink-0 rounded-full bg-gray-800 p-1 text-gray-400 hover:text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800">
              <span class="absolute -inset-1.5"></span>
              <span class="sr-only">View notifications</span>
              <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                <path stroke-linecap="round" stroke-linejoin="round" d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0" />
              </svg>
            </button>
  
            <!-- Profile dropdown -->
            <div class="relative ml-4 flex-shrink-0">
              <div>
                
                <button type="button" class="relative flex rounded-full bg-gray-800 text-sm text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800" id="user-menu-button" aria-expanded="false" aria-haspopup="true">
                  <span class="absolute -inset-1.5"></span>
                  <span class="sr-only">Open user menu</span>
                  <img class="h-8 w-8 rounded-full" src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="">
                </button>
        

              </div>
  
              <!--
                Dropdown menu, show/hide based on menu state.
  
                Entering: "transition ease-out duration-100"
                  From: "transform opacity-0 scale-95"
                  To: "transform opacity-100 scale-100"
                Leaving: "transition ease-in duration-75"
                  From: "transform opacity-100 scale-100"
                  To: "transform opacity-0 scale-95"
              -->
              
            </div>
          </div>
        </div>
      </div>
    </div>

    <main>
        <div class="mx-auto max-w-3xl px-4 sm:px-6 lg:max-w-7xl lg:px-8">
          <div class="py-24 text-center">
            <h1 class="text-4xl font-bold tracking-tight text-white">Class Photo Gallery</h1>
            <p class="mx-auto mt-4 max-w-3xl text-base text-white">Let's embark on this visual journey together and relive those unforgettable moments.</p>
          </div>
  
          <!-- Filters -->
          <section aria-labelledby="filter-heading" class="border-t border-gray-200 pt-6">
            <h2 id="filter-heading" class="sr-only">Product filters</h2>
  
            <div class="flex items-center justify-between">
              <div class="relative inline-block text-left">
               
  
                <!--
                  Dropdown menu, show/hide based on menu state.
  
                  Entering: "transition ease-out duration-100"
                    From: "transform opacity-0 scale-95"
                    To: "transform opacity-100 scale-100"
                  Leaving: "transition ease-in duration-75"
                    From: "transform opacity-100 scale-100"
                    To: "transform opacity-0 scale-95"
                -->
                
  
              <!-- Mobile filter dialog toggle, controls the 'mobileFilterDialogOpen' state. -->
              <button type="button" class="inline-block text-sm font-medium text-gray-700 hover:text-gray-900 sm:hidden">Filters</button>
  
              <div class="hidden sm:flex sm:items-baseline sm:space-x-8">
                <div id="menu" class="relative inline-block text-left">
                  
  
                  <!--
                    Entering: "transition ease-out duration-100"
                      From: "transform opacity-0 scale-95"
                      To: "transform opacity-100 scale-100"
                    Leaving: "transition ease-in duration-75"
                      From: "transform opacity-100 scale-100"
                      To: "transform opacity-0 scale-95"
                  -->
                  
  
                  <!--
                    Entering: "transition ease-out duration-100"
                      From: "transform opacity-0 scale-95"
                      To: "transform opacity-100 scale-100"
                    Leaving: "transition ease-in duration-75"
                      From: "transform opacity-100 scale-100"
                      To: "transform opacity-0 scale-95"
                  -->
                  
  
                  <!--
                    Entering: "transition ease-out duration-100"
                      From: "transform opacity-0 scale-95"
                      To: "transform opacity-100 scale-100"
                    Leaving: "transition ease-in duration-75"
                      From: "transform opacity-100 scale-100"
                      To: "transform opacity-0 scale-95"
                  -->
               
  
                  <!--
                    Entering: "transition ease-out duration-100"
                      From: "transform opacity-0 scale-95"
                      To: "transform opacity-100 scale-100"
                    Leaving: "transition ease-in duration-75"
                      From: "transform opacity-100 scale-100"
                      To: "transform opacity-0 scale-95"
                  -->
                  
          </section>
  
          <!-- Product grid -->
          <section aria-labelledby="products-heading" class="mt-8">
            <h2 id="products-heading" class="sr-only">Products</h2>
  
            <div class="grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-3 xl:gap-x-8">
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/2259997/pexels-photo-2259997.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Person using a pen to cross a task off a productivity paper card." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Abdul Rahman</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/5905436/pexels-photo-5905436.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Paper card sitting upright in walnut card holder on desk." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>sed do eiusmod tempor incididunt ut labore</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Tom Cook</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/3825456/pexels-photo-3825456.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Textured gray felt pouch for paper cards with snap button flap and elastic pen holder loop." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">John Davies</p>
              </a>
  
              <!-- More products... -->
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/5553640/pexels-photo-5553640.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Person using a pen to cross a task off a productivity paper card." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Techie</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/901964/pexels-photo-901964.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Paper card sitting upright in walnut card holder on desk." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Walnut</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/3747500/pexels-photo-3747500.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Textured gray felt pouch for paper cards with snap button flap and elastic pen holder loop." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Heather Gray</p>
              </a>
            </div>
          </section>
  
          <section aria-labelledby="featured-heading" class="relative mt-16 overflow-hidden rounded-lg lg:h-96">
            <div class="absolute inset-0">
              <img src="https://images.pexels.com/photos/6238056/pexels-photo-6238056.jpeg?auto=compress&cs=tinysrgb&w=600" alt="" class="h-full w-full object-cover object-center">
            </div>
            <div aria-hidden="true" class="relative h-96 w-full lg:hidden"></div>
            <div aria-hidden="true" class="relative h-32 w-full lg:hidden"></div>
            <div class="absolute inset-x-0 bottom-0 rounded-bl-lg rounded-br-lg bg-black bg-opacity-75 p-6 backdrop-blur backdrop-filter sm:flex sm:items-center sm:justify-between lg:inset-x-auto lg:inset-y-0 lg:w-96 lg:flex-col lg:items-start lg:rounded-br-none lg:rounded-tl-lg">
              <div>
                <h2 id="featured-heading" class="text-xl font-bold text-white">Gallery Collection</h2>
                <p class="mt-1 text-sm text-gray-300">Upgrade your desk with objects that keep you organized and clear-minded.</p>
              </div>
              <a href="#" class="mt-6 flex flex-shrink-0 items-center justify-center rounded-md border border-white border-opacity-25 bg-white bg-opacity-0 px-4 py-3 text-base font-medium text-white hover:bg-opacity-10 sm:ml-8 sm:mt-0 lg:ml-0 lg:w-full">View the collection</a>
            </div>
          </section>
  
          <section aria-labelledby="more-products-heading" class="mt-16 pb-24">
            <h2 id="more-products-heading" class="sr-only">More products</h2>
  
            <div class="grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-3 xl:gap-x-8">
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/5940856/pexels-photo-5940856.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Close up of long kettle spout pouring boiling water into pour-over coffee mug with frothy coffee." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p>❤️</p>
                </div>
                <p class="mt-1 text-sm italic text-white">Boyz</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/3403295/pexels-photo-3403295.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Extra large black leather workspace pad on desk with computer, wooden shelf, desk organizer, and computer peripherals." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Black</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/6238048/pexels-photo-6238048.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Leather long wallet held open with hand-stitched card dividers, full-length bill pocket, and simple tab closure." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Natural</p>
              </a>
  
              <!-- More products... -->
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/6627401/pexels-photo-6627401.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Person using a pen to cross a task off a productivity paper card." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">John Kamara</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/9431441/pexels-photo-9431441.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Paper card sitting upright in walnut card holder on desk." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Walnut</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/5905618/pexels-photo-5905618.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Textured gray felt pouch for paper cards with snap button flap and elastic pen holder loop." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Heather Gray</p>
              </a>

              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/4560148/pexels-photo-4560148.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Person using a pen to cross a task off a productivity paper card." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p>$13</p>
                </div>
                <p class="mt-1 text-sm italic text-white">Force</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/6281735/pexels-photo-6281735.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Paper card sitting upright in walnut card holder on desk." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Walnut</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/5905958/pexels-photo-5905958.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Textured gray felt pouch for paper cards with snap button flap and elastic pen holder loop." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Heather Gray</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/6281963/pexels-photo-6281963.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" alt="Person using a pen to cross a task off a productivity paper card." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p>❤️</p>
                </div>
                <p class="mt-1 text-sm italic text-white">Augusta Sesay</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/6334869/pexels-photo-6334869.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1" alt="Paper card sitting upright in walnut card holder on desk." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p>  </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Awesome</p>
              </a>
              <a href="#" class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg sm:aspect-h-3 sm:aspect-w-2">
                  <img src="https://images.pexels.com/photos/6333724/pexels-photo-6333724.jpeg?auto=compress&cs=tinysrgb&w=600" alt="Textured gray felt pouch for paper cards with snap button flap and elastic pen holder loop." class="h-full w-full object-cover object-center group-hover:opacity-75">
                </div>
                <div class="mt-4 flex items-center justify-between text-base font-medium text-white">
                  <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</h3>
                  <p> </p>
                </div>
                <p class="mt-1 text-sm italic text-white">Heather Gray</p>
              </a>
            </div>
          </section>
        </div>
      </main>
  
      <footer aria-labelledby="footer-heading" class="border-t border-gray-200 bg-white">
        <h2 id="footer-heading" class="sr-only">Footer</h2>
        <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
        
            <div class="grid grid-cols-1 md:grid-flow-col md:auto-rows-min md:grid-cols-12 md:gap-x-8 md:gap-y-16">
              <!-- Image section -->
              
          </div>
  
          <div class="border-t border-dark-900 py-10 text-center">
            <p class="text-sm text-gray-500">&copy; 2023 Your Company, Inc. All rights reserved.</p>
          </div>
        </div>
      </footer>

    
  
    <!-- Mobile menu, show/hide based on menu state. -->
    <div class="lg:hidden" id="mobile-menu">
      <div class="space-y-1 px-2 pb-3 pt-2">
        <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
        <a href="#" class="block rounded-md bg-gray-900 px-3 py-2 text-base font-medium text-white">Home</a>
        <a href="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Explore</a>
        <a href="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Universities</a>
        <a href="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white">License</a>
      </div>
      <a href="#" class="ml-6 inline-flex items-center rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Upload</a>
      <div class="border-t border-gray-700 pb-3 pt-4">
        <div class="flex items-center px-5">
          <div class="flex-shrink-0">
            <img class="h-10 w-10 rounded-full" src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="">
          </div>
          <div class="ml-3">
            <div class="text-base font-medium text-white">Tom Cook</div>
            <div class="text-sm font-medium text-gray-400">tom@example.com</div>
          </div>
          <button type="button" class="relative ml-auto flex-shrink-0 rounded-full bg-gray-800 p-1 text-gray-400 hover:text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800">
            <span class="absolute -inset-1.5"></span>
            <span class="sr-only">View notifications</span>
            <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M14.857 17.082a23.848 23.848 0 005.454-1.31A8.967 8.967 0 0118 9.75v-.7V9A6 6 0 006 9v.75a8.967 8.967 0 01-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 01-5.714 0m5.714 0a3 3 0 11-5.714 0" />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </nav>
  