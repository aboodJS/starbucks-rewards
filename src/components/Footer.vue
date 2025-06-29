<script setup>
import DropDown from './DropDown.vue'
</script>

<template>
  <footer class="h-fit grid gap-10">
    <section class="md:flex grid justify-evenly max-md:content-start max-md:gap-7">
      <DropDown title="About Us">
        <i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Our Company</a></i
        ><i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Our Coffee</a></i
        ><i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">About Starbucks</a></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >StarBucks Archive</a
          ></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >Investor Relations</a
          ></i
        >
        <i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Customer Service</a></i
        >
        <i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Contact Us</a></i>
      </DropDown>
      <DropDown title="Careers">
        <i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >Culture and Values</a
          ></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >Belonging at Starbucks</a
          ></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >College Achievement Plan</a
          ></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Alumni Community</a></i
        ><i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">US Careers</a></i>
        <i>
          <a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >International Careers</a
          >
        </i>
      </DropDown>
      <DropDown title="Social Impact">
        <i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Communities</a></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >StarBucks Foundation</a
          ></i
        ><i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Sustainability</a></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >Enviromental and Social Impact Reporting</a
          ></i
        >
      </DropDown>
      <DropDown title="For Business Partners">
        <i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >Landlord Support Center</a
          ></i
        ><i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Suppliers</a></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >Corporate Gift Card Sales</a
          ></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >Office and FoodService Coffee</a
          ></i
        >
      </DropDown>
      <DropDown title="Order and Pick Up">
        <i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Order on the App</a></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Order on the Web</a></i
        ><i><a class="text-[#B9B9B9] hover:text-black transition-all" href="">Delivery</a></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >Order and Pick Up Options</a
          ></i
        ><i
          ><a class="text-[#B9B9B9] hover:text-black transition-all" href=""
            >Explore and Find Coffee for Home</a
          ></i
        >
      </DropDown>
    </section>
    <hr class="text-[#e5e5e5]" />
    <section class="grid gap-7 justify-start ml-5">
      <ul class="flex justify-evenly w-1/4 max-md:gap-x-4">
        <li>
          <a href=""><i class="bx bxl-spotify text-4xl"></i></a>
        </li>
        <li>
          <a href=""><i class="bx bxl-facebook-circle text-4xl"></i></a>
        </li>
        <li>
          <a href=""><i class="bx bxl-pinterest text-4xl"></i></a>
        </li>
        <li>
          <a href=""><i class="bx bxl-instagram-alt text-4xl"></i></a>
        </li>
        <li>
          <a href=""><i class="bx bxl-youtube text-4xl"></i></a>
        </li>
        <li>
          <a href=""><i class="bx bxl-twitter text-4xl"></i></a>
        </li>
      </ul>
      <ul class="grid gap-5">
        <li><a class="hover:underline" href="">Privacy Notice</a></li>
        <li><a class="hover:underline" href="">Consumer Health Privacy Notice</a></li>
        <li><a class="hover:underline" href="">Terms of Use</a></li>
        <li><a class="hover:underline" href="">Do Not Share My Personal Information</a></li>
        <li><a class="hover:underline" href="">CA Supply Chain Act</a></li>
        <li><a class="hover:underline" href="">Accessibility</a></li>
        <li><a class="hover:underline" href="">Cookie Preferences</a></li>
      </ul>
      <p class="text-[#6b6b6b]">© 2025 Starbucks Coffee Company. All rights reserved.</p>
    </section>
  </footer>
</template>
