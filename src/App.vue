<script setup>
import { ref } from 'vue'
import Extra from './components/ExtraBox.vue'
import GetStarted from './components/getStarted.vue'
import NavBar from './components/NavBar.vue'
import RewardShocase from './components/rewardShocase.vue'
import SideBar from './components/SideBar.vue'
import PartnerBox from './components/PartnerBox.vue'
import Foot from './components/Footer.vue'
import Footer from './components/Footer.vue'
const visible = ref(false)
const boxVisible = ref(false)
const boxId = ref('')
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
    <section class="md:h-[70vh] max-md:h-fit grid md:mt-28">
      <div class="grid justify-center content-center gap-7">
        <h1 class="text-center text-2xl font-bold">Endless Extras</h1>
        <p class="w-3/4 text-center justify-self-center">
          Joining Starbucks® Rewards means unlocking access to benefits like quick and easy
          ordering, tasty Rewards and—yes, free coffee.
        </p>
      </div>
      <div
        :class="['absolute h-28 w-28 bg-[#ffffff] z-10', boxVisible ? 'grid' : 'hidden h-0 w-0']"
      >
        {{ boxId }}
      </div>
      <main class="md:flex justify-center max-md:grid max-md:text-md md:gap-7 justify-self-center">
        <Extra
          @show-box="
            () => {
              boxVisible = !boxVisible
              console.log(boxVisible)
            }
          "
          unique-id="1"
          title="Fun freebies"
          image="https://www.starbucks.com/weblx/images/rewards/benefits/1-fun-freebies.jpg"
          >Not only can you earn free food, drinks and more, look forward to a birthday treat on
          us.</Extra
        >
        <Extra
          @show-box="
            () => {
              boxVisible = !boxVisible
              console.log(boxVisible)
            }
          "
          unique-id="2"
          title="Order & pay ahead"
          image="https://www.starbucks.com/weblx/images/rewards/benefits/2-order-and-pay-ahead.jpg"
          >Master the art of ordering ahead with saved favorites and payment methods.</Extra
        >
        <Extra
          @show-box="
            () => {
              boxVisible = !boxVisible
              console.log(boxVisible)
            }
          "
          unique-id="3"
          title="Get to free faster"
          image="https://www.starbucks.com/weblx/images/rewards/benefits/3-get-to-free-faster.jpg"
          >Earn Stars even quicker with Bonus Star challenges, Double Star Days and exciting
          games.</Extra
        >
      </main>
    </section>
    <section class="bg-[#f2f0eb] grid content-evenly gap-5 pb-10">
      <div class="grid justify-center text-center mb-12">
        <h1 class="md:text-2xl font-bold text-[#1f1f1e]">Cash or card, you earn Stars</h1>
        <p class="w-3/4 text-center justify-self-center">
          No matter how you pay, you can earn Stars with your morning coffee. Those Stars add up to
          (really delicious) Rewards.
        </p>
      </div>
      <div class="md:flex max-md:grid text-[#1f1f1e] ml-5 justify-self-center">
        <div class="mb-10">
          <h1 class="md:text-2xl font-bold">1★Star per dollar</h1>
          <p>Pay as you go</p>
        </div>
        <div class="flex w-fit">
          <img
            src="https://www.starbucks.com/weblx/images/rewards/ways-to-pay/1A.png"
            alt=""
            class="h-[158px] w-[112px]"
          />
          <div>
            <h1 class="h-fit font-bold mb-5">Scan and pay separately</h1>
            <p class="row-span-1 w-3/4 max-md:text-sm">
              Use cash or credit/debit card at the register.
            </p>
          </div>
        </div>

        <div class="flex w-fit">
          <img
            src="https://www.starbucks.com/weblx/images/rewards/ways-to-pay/1B.png"
            alt=""
            class="h-[158px] w-[112px]"
          />
          <div>
            <h1 class="h-fit font-bold mb-5">Save payment in the app</h1>
            <p class="row-span-1 w-3/4 max-md:text-sm">
              Check-out faster by saving a credit/debit card or PayPal to your account. You’ll be
              able to order ahead or scan and pay at the register in one step.
            </p>
          </div>
        </div>
      </div>
      <hr class="text-[#d9d8d3] w-[90%] justify-self-center my-4" />
      <div class="md:flex max-md:grid text-[#1f1f1e] justify-self-center ml-5">
        <div class="mb-10">
          <h1 class="md:text-2xl font-bold">2★Stars per dollar</h1>
          <p>Add funds in the app</p>
        </div>
        <div class="flex w-fit">
          <img
            src="https://www.starbucks.com/weblx/images/rewards/ways-to-pay/2A.png"
            alt=""
            class="h-[158px] w-[112px]"
          />
          <div class="w-70 h-fit">
            <h1 class="h-fit font-bold mb-5 w-fit">Preload</h1>
            <p class="max-md:text-sm">
              To save time and earn Stars twice as fast, add money to your digital Starbucks Card
              using any payment option. Scan and pay in one step or order ahead in the app.
            </p>
          </div>
        </div>

        <div class="flex w-fit">
          <img
            src="https://www.starbucks.com/weblx/images/rewards/ways-to-pay/2B.png"
            alt=""
            class="h-[158px] w-[112px]"
          />
          <div>
            <h1 class="h-fit font-bold mb-5">Register your gift card</h1>
            <p class="row-span-1 w-3/4 max-md:text-sm">
              Then use it to pay through the app. You can even consolidate balances from multiple
              cards in one place.
            </p>
          </div>
        </div>
      </div>
    </section>
    <section
      id="partner-rewards"
      class="bg-[#0f4c3a] h-[90vh] grid justify-center content-center max-md:mt-12"
    >
      <div class="w-[95vw] h-[80vh] bg-[#d4e9e2] grid max-md:h-fit max-md:w-screen">
        <div class="text-center h-28 grid justify-center content-center gap-6">
          <h1 class="text-2xl font-bold">Keep the Rewards Coming</h1>
          <p class="font-semibold max-md:text-sm">
            The Rewards don't stop at your morning coffee. Join Starbucks® Rewards and unlock perks
            from our partners, all while earning more Stars.
          </p>
        </div>
        <div class="md:flex max-md:grid max-md:gap-3 justify-evenly">
          <PartnerBox
            img="https://www.starbucks.com/weblx/images/rewards/loyalty-partnerships/delta-skymiles.png"
            name="Delta SkyMiles"
            >and Starbucks® Rewards accounts to earn miles on Starbucks Card reloads of $25 or
            more, plus Double Stars on travel days.1</PartnerBox
          >
          <PartnerBox
            img="https://www.starbucks.com/weblx/images/rewards/loyalty-partnerships/bank-of-america.png"
            name="Bank Of America"
            >eligible card and Starbucks® Rewards account to earn 2% Cash Back and Bonus Stars on
            qualifying Starbucks in-app purchases.2</PartnerBox
          >
          <PartnerBox
            img="https://www.starbucks.com/weblx/images/rewards/loyalty-partnerships/marriott-bonvoy/marriott-logo.png"
            name="Marriot Bonvoy"
          >
            and Starbucks® Rewards accounts to earn Double Stars during eligible stays, points
            during any Marriott Bonvoy Week and more.3
          </PartnerBox>
        </div>
        <button
          class="font-bold bg-[#046241] p-2 rounded-3xl text-white justify-self-center h-fit mt-10"
        >
          Join Starbucks® Rewards
        </button>
      </div>
    </section>
    <div class="h-72 max-md:ml-4 grid content-center justify-center">
      <span class="grid w-fit justify-self-center">
        <h1 class="text-2xl font-bold">Questions?</h1>
        <p class="text-sm grid justify-center">
          We want to help in any way we can. You can ask your barista anytime or we’ve answered the
          most commonly asked terms <a href="#" class="text-[#046241] underline">right over here</a>
        </p>
      </span>
    </div>
    <section class="h-fit bg-[#F9F9F9] w-screen mb-12">
      <p class="text-xs grid gap-5 w-screen mb-12">
        <i>At participating stores. Restrictions apply. </i
        ><i>
          1Excludes taxes and gratuities. At participating stores. Some restrictions apply. Flights
          purchased close to departure may not earn double Stars. Stars and miles may not be earned
          on purchases of alcohol, Starbucks Cards and Starbucks Card reloads. For details, visit
          <a href="#" class="text-[#04754A] underline">deltastarbucks.com/terms</a>
        </i>
        <i
          >2At participating stores only. Some restrictions apply. Linked Card members will earn 2%
          Cash Back on the full purchase price of every Qualifying Purchase. Extra Star offer
          excludes taxes and tips. Stars may not be earned on purchases of alcohol or on reloads of
          Starbucks Cards that are not registered. For details, visit
          <a href="#" class="text-[#04754A] underline">Terms and Conditions</a> . Bank of America,
          N.A. Member FDIC</i
        ><i
          >3Individuals must link loyalty program accounts to participate in offer. Members with
          linked accounts will earn: (a) double Starbucks Rewards Stars on Qualifying Starbucks
          Transactions during Eligible Stays at Participating Marriott Bonvoy Hotels, excluding
          stays at Homes & Villas by Marriott Bonvoy and The Ritz-Carlton Yacht Collection, and (b)
          earn 100 Marriott Bonvoy Points upon completion of 3 Qualifying Starbucks Transactions
          during Marriott Bonvoy Week. Qualifying Starbucks Transactions must be made at U.S.
          participating Starbucks stores and exclude purchases of alcoholic beverages, Starbucks
          Card eGifts and physical Starbucks gift. To earn Double Stars, the applicable stay must
          qualify as an Eligible Stay at a Participating Marriott Bonvoy® Hotel under offer terms
          and conditions. Other restrictions and exclusions apply. For full offer terms and
          conditions, visit
          <a href="#" class="text-[#04754A] underline"> Starbucks.com/MarriottBonvoy </a>
          . Marriott Bonvoy® and its affiliated brands and hotels are the registered trademarks
          and/or service marks of Marriott International, Inc. and its affiliates. Used under
          license from Marriott International, Inc.↩
        </i>
      </p>
      <main class="grid md:grid-cols-2 md:grid-rows-2 gap-x-5 max-md:gap-5 max-md:text-sm">
        <div class="grid gap-5 content-center">
          <h1 class="text-[#686868] font-bold">Earning Stars</h1>
          <p>
            Stars cannot be earned on purchases of alcohol, Starbucks Cards or Starbucks Card
            reloads.
          </p>
          <p>
            Earn 1 Star per $1 spent when you scan your member barcode in the app, then pay with
            cash, credit/debit cards or mobile wallets at participating stores. You can also earn 1
            Star per $1 spent when you link a payment method and pay directly through the app.
          </p>
          <p>
            Earn 2 Stars per $1 spent when you load funds and pay with your digital Starbucks Card
            in the app. You can also earn 2 Stars per $1 spent when you pay in-person at a
            participating store with your registered physical Starbucks Card or scan your member
            barcode in the app, and then use any physical Starbucks Card (regardless of whether it
            is registered) to complete the purchase.
          </p>
        </div>
        <div class="grid gap-5 content-center">
          <h1 class="text-[#686868] font-bold">Terms of Use</h1>
          <p>
            For full program details visit
            <a href="#" class="text-[#04754A] underline"> starbucks.com/rewards/terms </a>
          </p>
          <p>
            Starbucks® Rewards benefits are available at participating Starbucks stores. Not all
            stores have the ability to honor Rewards at this time. Visit the
            <a href="#" class="text-[#04754A] underline"> Starbucks Store Locator</a> and search for
            locations honoring “Redeem Rewards”.
          </p>
        </div>
        <div class="grid gap-5 content-center">
          <h1 class="text-[#686868] font-bold">Benefits</h1>
          <p>
            Free refills available during same in-store visit only. To qualify for the Birthday
            Reward, you must have made at least one Star-earning transaction.
          </p>
        </div>
        <div class="grid gap-5 content-center">
          <h1 class="text-[#686868] font-bold">Redeeming Rewards</h1>
          <p>
            Rewards cannot be redeemed for alcoholic beverages or multi-serve items. You pay the
            difference for any beverage customization over $1 and/or merchandise item over $20. Not
            all stores honor tiered Rewards. Select stores redeem 200 Stars for free food or drink
            items only.
          </p>
        </div>
      </main>
    </section>
    <Foot></Foot>
  </main>
</template>

<style>
#partner-rewards {
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='18' viewBox='0 0 100 18'%3E%3Cpath fill='%23046241' fill-opacity='1' d='M61.82 18c3.47-1.45 6.86-3.78 11.3-7.34C78 6.76 80.34 5.1 83.87 3.42 88.56 1.16 93.75 0 100 0v6.16C98.76 6.05 97.43 6 96 6c-9.59 0-14.23 2.23-23.13 9.34-1.28 1.03-2.39 1.9-3.4 2.66h-7.65zm-23.64 0H22.52c-1-.76-2.1-1.63-3.4-2.66C11.57 9.3 7.08 6.78 0 6.16V0c6.25 0 11.44 1.16 16.14 3.42 3.53 1.7 5.87 3.35 10.73 7.24 4.45 3.56 7.84 5.9 11.31 7.34zM61.82 0h7.66a39.57 39.57 0 0 1-7.34 4.58C57.44 6.84 52.25 8 46 8S34.56 6.84 29.86 4.58A39.57 39.57 0 0 1 22.52 0h15.66C41.65 1.44 45.21 2 50 2c4.8 0 8.35-.56 11.82-2z'%3E%3C/path%3E%3C/svg%3E");
}
</style>
