<template>
  <nav class="flex justify-between items-center h-28">
    <div class="flex items-center w-96 mx-3">
      <div class="h-14 w-14 bg-green-700"></div>
      <ul class="flex justify-around w-72">
        <li class="text-[15px] font-semibold hover:text-green-700 transition-colors cursor-pointer">
          MENU
        </li>
        <li class="text-[15px] font-semibold hover:text-green-700 transition-colors cursor-pointer">
          REWARDS
        </li>
        <li class="text-[15px] font-semibold hover:text-green-700 transition-colors cursor-pointer">
          GIFT CARDS
        </li>
      </ul>
    </div>
    <div>
      <div class="flex items-center w-96 justify-around">
        <div class="flex hover:text-green-700 transition-colors cursor-pointer">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            style="fill: rgba(0, 0, 0, 1); transform:; msfilter:"
          >
            <path
              d="M12 22s8.029-5.56 8-12c0-4.411-3.589-8-8-8S4 5.589 4 9.995C3.971 16.44 11.696 21.784 12 22zM8 9h3V6h2v3h3v2h-3v3h-2v-3H8V9z"
            ></path>
          </svg>
          <p class="font-semibold hover:text-green-700 transition-colors">Find a store</p>
        </div>
        <div class="flex justify-between w-40">
          <button class="border-[1px] rounded-2xl py-1 px-3 hover:bg-slate-200 transition-colors">
            sign in
          </button>
          <button class="rounded-2xl py-1 px-3 bg-black text-white hover:opacity-70 transition-all">
            log in
          </button>
          <i class="bxr bx-menu-close" style="color: #6b6b6b" />
        </div>
      </div>
    </div>
  </nav>
  <div class="bg-[#1e3932] text-white h-10 flex items-center sticky top-0 w-full">
    <p class="pl-24">STARBUCKS&reg; REWARDS</p>
  </div>
</template>
