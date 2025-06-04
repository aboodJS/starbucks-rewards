<script setup>
import { ref } from 'vue'
import Extra from './components/ExtraBox.vue'
import GetStarted from './components/getStarted.vue'
import NavBar from './components/NavBar.vue'
import RewardShocase from './components/rewardShocase.vue'
import SideBar from './components/SideBar.vue'
const visible = ref(false)
</script>

<template>
  <main :class="[visible ? 'fixed -top-0 overflow-hidden' : '']">
    <NavBar>
      <img
        class="md:hidden"
        src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACQAAAAkCAYAAADhAJiYAAAA6UlEQVRYR+2WYQrDIAxG49hp9RK7hJ521KWMwmTRbyYTWkj/FBptnk+TNtDJrnAyHnIgtCNuyA0hAyh+nTOUUqriajZ+emsjwiMkgnLOooyuoS4Qp9pJrWr/A3So4HtlSxaoaSDofNEAyyKXIDkQ0to1FGN8oMlEdx7ylIcNQvuEUor4/t/LvlPr2hYwXWUpcmP8xBW7n6YlvoVOA7Vb1kusB5reMnx+1ozwskder2MopcgVbeMdtYTpKjt+P9o6+k5RaaMw/PTLWGogtOfa+DSQNpF1nu2QWLML8x0ISXVDbggZQPHTnaEXjxY9JQpI6jIAAAAASUVORK5CYII="
        @click="
          () => {
            visible = !visible
            console.log(visible)
          }
        "
      />
    </NavBar>
    <SideBar v-model="visible"></SideBar>
    <div
      class="bg-[#1e3932] text-white h-10 max-md:h-14 flex items-center max-md:justify-between sticky top-0 w-screen z-0"
    >
      <p class="md:pl-24 max-md:w-1/3">STARBUCKS&reg; REWARDS</p>
      <button class="md:hidden border-1 rounded-3xl py-1 px-2">Join in the app</button>
    </div>
    <section
      class="flex min-md:justify-evenly h-[67vh] items-center bg-[#fbf5e8] max-md:grid max-md:h-fit max-md:text-center max-md:justify-center"
    >
      <div class="grid gap-5 md:ml-16 max-md:mt-6">
        <h1 class="text-5xl font-bold text-[#32462f] md:w-9/12 max-md:text-2xl">
          It's a great day for free coffee
        </h1>
        <p>Sign up and start enjoying the perks of Starbucks® Rewards.</p>
        <button
          class="bg-[#00754a] h-10 w-24 text-white rounded-3xl py-1 px-3 hover:bg-green-800 transition-colors max-md:justify-self-center max-md:hidden cursor-pointer"
        >
          Join now
        </button>
        <button
          class="bg-[#00754a] h-10 w-24 max-md:w-36 text-white rounded-3xl py-1 px-3 hover:bg-green-800 transition-colors max-md:justify-self-center md:hidden"
        >
          Join in the app
        </button>

        <p class="max-md:hidden">
          It's even better with <a href="#" class="underline">the app</a>.
        </p>
        <p class="md:hidden"><a href="#" class="underline">or join online</a>.</p>
      </div>
      <img
        src="./assets/pexels-chiecharon-1193335.jpg"
        alt=""
        class="md:w-1/2 h-[67vh] max-md:mt-7"
      />
    </section>
    <section class="grid content-center md:justify-center gap-5 my-16">
      <div class="text-center grid gap-5">
        <h1 class="text-3xl font-bold">Getting started is easy</h1>
        <p>Earn Stars and get rewarded in a few easy steps.</p>
      </div>
      <main class="md:flex justify-center max-md:grid gap-7">
        <GetStarted title="Create an account" number="1"
          >To get started, join now. You can also Join in the app to get access to the full range of
          Starbucks® Rewards benefits.</GetStarted
        >
        <GetStarted title="Order and pay how you’d like" number="2"
          >Use cash, credit/debit card or save some time and pay right through the app. You’ll
          collect Stars all ways. Learn how</GetStarted
        >
        <GetStarted title="Earn Stars, get Rewards" number="3"
          >As you earn Stars, you can redeem them for Rewards—like free food, drinks, and more.
          Start redeeming with as little as 25 Stars!</GetStarted
        >
      </main>
    </section>
    <RewardShocase></RewardShocase>
    <section class="h-[70vh] grid mt-28">
      <div class="grid justify-center content-center gap-7">
        <h1 class="text-center text-2xl font-bold">Endless Extras</h1>
        <p class="w-3/4 text-center justify-self-center">
          Joining Starbucks® Rewards means unlocking access to benefits like quick and easy
          ordering, tasty Rewards and—yes, free coffee.
        </p>
      </div>
      <main class="md:flex justify-center max-md:grid gap-7 justify-self-center">
        <Extra
          title="Fun freebies"
          image="https://www.starbucks.com/weblx/images/rewards/benefits/1-fun-freebies.jpg"
          >Not only can you earn free food, drinks and more, look forward to a birthday treat on
          us.</Extra
        >
        <Extra
          title="Order & pay ahead"
          image="https://www.starbucks.com/weblx/images/rewards/benefits/2-order-and-pay-ahead.jpg"
          >Master the art of ordering ahead with saved favorites and payment methods.</Extra
        >
        <Extra
          title="Get to free faster"
          image="https://www.starbucks.com/weblx/images/rewards/benefits/3-get-to-free-faster.jpg"
          >Earn Stars even quicker with Bonus Star challenges, Double Star Days and exciting
          games.</Extra
        >
      </main>
    </section>

    <section class="bg-[#f2f0eb] h-fit grid grid-cols-4 grid-rows-3 mt-28">
      <div class="col-span-full justify-self-center text-center grid content-evenly">
        <h1 class="text-2xl font-bold justify-self-center">Cash or card, you earn Stars</h1>
        <p class="text-md w-3/4 justify-self-center">
          No matter how you pay, you can earn Stars with your morning coffee. Those Stars add up to
          (really delicious) Rewards.
        </p>
      </div>
      <div class="grid grid-rows-1 grid-cols-3 col-span-3">
        <div class="ml-10">
          <h1 class="text-2xl font-bold">1★Star per dollar</h1>
          <p>Pay as you go</p>
        </div>
        <div class="grid grid-cols-2 grid-rows-2 justify-center content-center">
          <img
            src="https://www.starbucks.com/weblx/images/rewards/ways-to-pay/1A.png"
            class="h-44 row-span-2 self-center"
            alt=""
          />
          <h1 class="text-2xl font-bold col-start-2">Scan and pay separately</h1>
          <p class="col-start-2 text-[14px]">Use cash or credit/debit card at the register.</p>
        </div>
        <div class="grid grid-cols-2 grid-rows-2 justify-center">
          <img
            src="https://www.starbucks.com/weblx/images/rewards/ways-to-pay/1B.png"
            class="h-44 row-span-2 self-center"
            alt=""
          />
          <h1 class="text-2xl font-bold col-start-2 self-center">Save payment in the app</h1>
          <p class="col-start-2 text-[14px] self-center">
            Check-out faster by saving a credit/debit card or PayPal to your account. You’ll be able
            to order ahead or scan and pay at the register in one step.
          </p>
        </div>
      </div>
      <div class="grid grid-rows-1 grid-cols-3 col-span-3">
        <div class="ml-10">
          <h1 class="text-2xl font-bold">2★Stars per dollar</h1>
          <p>Add funds in the app</p>
        </div>
        <div class="grid grid-cols-2 grid-rows-2 justify-center">
          <img
            src="https://www.starbucks.com/weblx/images/rewards/ways-to-pay/2A.png"
            class="h-44 row-span-2 self-center"
            alt=""
          />
          <h1 class="text-2xl font-bold col-start-2 self-center">Preload</h1>
          <p class="col-start-2 self-center text-[14px]">
            To save time and earn Stars twice as fast, add money to your digital Starbucks Card
            using any payment option. Scan and pay in one step or order ahead in the app.
          </p>
        </div>
        <div class="grid grid-cols-2 grid-rows-2 justify-center">
          <img
            src="https://www.starbucks.com/weblx/images/rewards/ways-to-pay/2B.png"
            class="h-44 row-span-2 self-center"
            alt=""
          />
          <h1 class="text-2xl font-bold col-start-2 self-center">Register your gift card</h1>
          <p class="col-start-2 self-center text-[14px]">
            Then use it to pay through the app. You can even consolidate balances from multiple
            cards in one place.
          </p>
        </div>
      </div>
    </section>
  </main>
</template>
