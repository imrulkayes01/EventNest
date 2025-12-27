<template>
  <header
    class="w-full bg-black/60 backdrop-blur-xl fixed top-0 z-50 border-b border-white/5"
  >
    <div
      class="absolute inset-0 bg-gradient-to-r from-transparent via-white/5 to-transparent pointer-events-none"
    ></div>
    <nav
      class="max-w-[1280px] mx-auto w-full flex items-center justify-between px-5 md:px-10 py-4 relative z-10"
    >
      <NuxtLink
        to="/"
        class="flex items-center gap-2 text-2xl font-bold cursor-pointer text-white tracking-tight"
      >
        <div class="flex flex-col gap-1.5">
          <div class="w-8 h-1 bg-[#07B300] rounded-full"></div>
          <div class="w-6 h-1 bg-[#07B300] rounded-full"></div>
          <div class="w-8 h-1 bg-[#07B300] rounded-full"></div>
        </div>
        EventFlow
      </NuxtLink>

      <!-- Desktop Menu -->
      <ul class="hidden lg:flex gap-6 text-lg font-medium text-gray-300">
        <NuxtLink
          to="/discover"
          class="hover:text-[#07B300] transition cursor-pointer"
          >Discover</NuxtLink
        >
        <NuxtLink
          to="/validate-ticket"
          class="hover:text-[#07B300] transition cursor-pointer"
        >
          Validate Ticket
        </NuxtLink>
        <NuxtLink
          to="/for-organizers"
          class="hover:text-[#07B300] transition cursor-pointer"
        >
          For Organizers
        </NuxtLink>
        <NuxtLink
          to="/about"
          class="hover:text-[#07B300] transition cursor-pointer"
          >About</NuxtLink
        >
        <NuxtLink
          to="/#how-it-works"
          class="hover:text-[#07B300] transition cursor-pointer"
        >
          How It Works
        </NuxtLink>
        <NuxtLink
          to="/#pricing"
          class="hover:text-[#07B300] transition cursor-pointer"
          >Pricing</NuxtLink
        >
      </ul>

      <div class="hidden lg:flex items-center gap-4">
        <button
          class="bg-[#22c55e]/10 hover:bg-[#22c55e]/20 text-white transition px-5 py-2.5 rounded-[0.50rem] font-bold text-lg"
        >
          Log In
        </button>
        <button
          class="bg-[#07B300] hover:bg-[#16a34a] transition px-5 py-2.5 text-black rounded-[0.50rem] font-bold text-lg"
        >
          Get Started
        </button>
      </div>

      <button @click="isMenuOpen = !isMenuOpen" class="lg:hidden text-white">
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
  </header>

  <!-- Mobile Menu Overlay -->
  <div
    v-if="isMenuOpen"
    class="fixed inset-0 bg-black/95 backdrop-blur-xl z-[100] flex flex-col items-center justify-center gap-8 lg:hidden transition-all duration-300"
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
        class="lucide lucide-x size-4"
        aria-hidden="true"
      >
        <path d="M18 6 6 18"></path>
        <path d="m6 6 12 12"></path>
      </svg>
    </button>
    <ul class="flex flex-col items-center gap-6 text-xl text-gray-300">
      <NuxtLink
        to="/discover"
        class="hover:text-[#22c55e] cursor-pointer"
        @click="isMenuOpen = false"
      >
        Discover
      </NuxtLink>
      <NuxtLink
        to="/validate-ticket"
        class="hover:text-[#22c55e] cursor-pointer"
        @click="isMenuOpen = false"
      >
        Validate Ticket
      </NuxtLink>
      <NuxtLink
        to="/for-organizers"
        class="hover:text-[#22c55e] cursor-pointer"
        @click="isMenuOpen = false"
      >
        For Organizers
      </NuxtLink>
      <NuxtLink
        to="/about"
        class="hover:text-[#22c55e] cursor-pointer"
        @click="isMenuOpen = false"
      >
        About
      </NuxtLink>
      <NuxtLink
        to="/#how-it-works"
        class="hover:text-[#22c55e] cursor-pointer"
        @click="isMenuOpen = false"
      >
        How It Works
      </NuxtLink>
      <NuxtLink
        to="/#pricing"
        class="hover:text-[#22c55e] cursor-pointer"
        @click="isMenuOpen = false"
      >
        Pricing
      </NuxtLink>
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
</template>

<style scoped></style>

<script setup>
import { ref } from "vue";

const isMenuOpen = ref(false);
</script>
