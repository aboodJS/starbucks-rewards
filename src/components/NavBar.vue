<template>
  <nav class="flex justify-between items-center h-28 w-screen overflow-x-hidden">
    <div class="h-14 w-14 bg-green-700 md:hidden"></div>
    <img
      class="md:hidden"
      src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACQAAAAkCAYAAADhAJiYAAAA6UlEQVRYR+2WYQrDIAxG49hp9RK7hJ521KWMwmTRbyYTWkj/FBptnk+TNtDJrnAyHnIgtCNuyA0hAyh+nTOUUqriajZ+emsjwiMkgnLOooyuoS4Qp9pJrWr/A3So4HtlSxaoaSDofNEAyyKXIDkQ0to1FGN8oMlEdx7ylIcNQvuEUor4/t/LvlPr2hYwXWUpcmP8xBW7n6YlvoVOA7Vb1kusB5reMnx+1ozwskder2MopcgVbeMdtYTpKjt+P9o6+k5RaaMw/PTLWGogtOfa+DSQNpF1nu2QWLML8x0ISXVDbggZQPHTnaEXjxY9JQpI6jIAAAAASUVORK5CYII="
    />
    <div class="flex items-center mx-3 max-md:hidden">
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
    <div class="max-md:hidden">
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
          <button
            class="border-[1px] rounded-2xl py-1 px-3 hover:bg-slate-200 transition-colors cursor-pointer"
          >
            sign in
          </button>
          <button
            class="rounded-2xl py-1 px-3 bg-black text-white hover:opacity-70 transition-all cursor-pointer"
          >
            log in
          </button>
        </div>
      </div>
    </div>
  </nav>
  <div
    class="bg-[#1e3932] text-white h-10 max-md:h-14 flex items-center max-md:justify-between sticky top-0 w-screen"
  >
    <p class="md:pl-24 max-md:w-1/3">STARBUCKS&reg; REWARDS</p>
    <button class="md:hidden border-1 rounded-3xl py-1 px-2">Join in the app</button>
  </div>
  <aside class="bg-white w-[70vw] h-[50%] -right-10 absolute">
    <ul class="grid h-36 gap-8 mt-10 justify-center w-28">
      <li>Menu</li>
      <li>Rewards</li>
      <li>Gift Cards</li>
    </ul>
    <div class="grid">
      <hr class="my-8 w-[70%] justify-self-center text-[#e5e5e5]" />
    </div>
    <div class="ml-8">
      <button
        class="mr-3 border-[1px] rounded-2xl py-1 px-3 hover:bg-slate-200 transition-colors cursor-pointer"
      >
        Sign in</button
      ><button
        class="rounded-2xl py-1 px-3 bg-black text-white hover:opacity-70 transition-all cursor-pointer"
      >
        Join now
      </button>
    </div>
    <div class="flex hover:text-green-700 transition-colors cursor-pointer ml-8 mt-5">
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
  </aside>
</template>
