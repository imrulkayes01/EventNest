<template>
  <section>
    <!-- Navbar -->
    <nav
      class="w-full flex items-center justify-between px-5 md:px-10 py-4 max-w-[1280px] mx-auto bg-black/50 backdrop-blur-md sticky top-0 z-50"
    >
      <div
        class="flex items-center gap-2 text-2xl font-[700] cursor-pointer text-white tracking-tight"
      >
        <span>
          <span class="text-[#22c55e]"
            ><svg
              xmlns="http://www.w3.org/2000/svg"
              width="32"
              height="32"
              viewBox="0 0 24 24"
              fill="currentColor"
              class="lucide lucide-layers"
            >
              <path
                d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                fill="none"
              />
            </svg>
          </span>
        </span>
        EventNest
      </div>

      <!-- Desktop Menu -->
      <ul class="hidden md:flex gap-6 text-sm font-medium text-gray-300">
        <li class="hover:text-[#16A34A] transition cursor-pointer">Discover</li>
        <li class="hover:text-[#16A34A] transition cursor-pointer">
          Validate Ticket
        </li>
        <li class="hover:text-[#16A34A] transition cursor-pointer">
          For Organizers
        </li>
        <li class="hover:text-[#16A34A] transition cursor-pointer">About</li>
        <li class="hover:text-[#16A34A] transition cursor-pointer">
          How It Works
        </li>
        <li class="hover:text-[#16A34A] transition cursor-pointer">Pricing</li>
      </ul>

      <div class="hidden md:flex items-center gap-4">
        <button
          class="bg-[#22c55e]/10 hover:bg-[#22c55e]/20 text-white transition px-5 py-2.5 rounded-[0.50rem] font-bold text-sm"
        >
          Log In
        </button>
        <button
          class="bg-[#22c55e] hover:bg-[#16a34a] transition px-5 py-2.5 text-black rounded-[0.50rem] font-bold text-sm"
        >
          Get Started
        </button>
      </div>

      <button @click="isMenuOpen = !isMenuOpen" class="md:hidden text-white">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="28"
          height="28"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="lucide lucide-menu"
        >
          <line x1="4" x2="20" y1="12" y2="12" />
          <line x1="4" x2="20" y1="6" y2="6" />
          <line x1="4" x2="20" y1="18" y2="18" />
        </svg>
      </button>
    </nav>

    <!-- Mobile Menu Overlay -->
    <div
      v-if="isMenuOpen"
      class="fixed inset-0 bg-black/95 backdrop-blur-xl z-50 flex flex-col items-center justify-center gap-8 md:hidden transition-all duration-300"
    >
      <button
        @click="isMenuOpen = false"
        class="absolute top-6 right-5 p-1 rounded-xl border-2 border-[#22c55e] text-gray-300 hover:text-white hover:bg-[#22c55e]/10 transition"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="lucide lucide-x"
        >
          <path d="M18 6 6 18" />
          <path d="m6 6 18 12" />
        </svg>
      </button>
      <ul class="flex flex-col items-center gap-6 text-xl text-gray-300">
        <li
          class="hover:text-[#22c55e] cursor-pointer"
          @click="isMenuOpen = false"
        >
          Discover
        </li>
        <li
          class="hover:text-[#22c55e] cursor-pointer"
          @click="isMenuOpen = false"
        >
          Validate Ticket
        </li>
        <li
          class="hover:text-[#22c55e] cursor-pointer"
          @click="isMenuOpen = false"
        >
          For Organizers
        </li>
        <li
          class="hover:text-[#22c55e] cursor-pointer"
          @click="isMenuOpen = false"
        >
          About
        </li>
        <li
          class="hover:text-[#22c55e] cursor-pointer"
          @click="isMenuOpen = false"
        >
          How It Works
        </li>
        <li
          class="hover:text-[#22c55e] cursor-pointer"
          @click="isMenuOpen = false"
        >
          Pricing
        </li>
      </ul>
      <div class="flex flex-col items-center gap-4 w-full px-10">
        <button
          class="w-full bg-[#22c55e]/10 hover:bg-[#22c55e]/20 text-white transition px-8 py-3 rounded-[0.50rem] font-bold text-lg"
          @click="isMenuOpen = false"
        >
          Log In
        </button>
        <button
          class="w-full bg-[#22c55e] hover:bg-[#16a34a] transition px-8 py-3 rounded-[0.50rem] text-black font-bold text-lg"
          @click="isMenuOpen = false"
        >
          Get Started
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped></style>

<script setup>
import { ref } from "vue";

const isMenuOpen = ref(false);
</script>
