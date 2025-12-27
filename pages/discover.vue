<template>
  <div class="min-h-screen bg-black text-white pt-24 pb-20">
    <div class="max-w-[1280px] mx-auto px-5 md:px-10">
      <!-- Hero Section -->
      <div class="mb-12 text-center md:text-left">
        <h1
          class="text-4xl md:text-7xl font-bold mb-6 tracking-tight leading-tight"
        >
          Discover
          <span class="text-[#07B300]">Amazing Events</span>
        </h1>
        <p class="text-gray-400 text-lg md:text-2xl max-w-2xl leading-relaxed">
          Find concerts, conferences, workshops, and more happening near you or
          online.
        </p>
      </div>

      <!-- Search & Filters -->
      <div class="space-y-6 mb-12">
        <div class="flex flex-col md:flex-row gap-3">
          <!-- Main Search -->
          <div class="flex-grow relative group">
            <div
              class="absolute inset-y-0 left-4 flex items-center pointer-events-none"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="20"
                height="20"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="text-gray-500 group-focus-within:text-[#07B300] transition-colors"
              >
                <circle cx="11" cy="11" r="8" />
                <path d="m21 21-4.3-4.3" />
              </svg>
            </div>
            <input
              type="text"
              placeholder="Search events..."
              class="w-full bg-[#0A0A0A] border border-white/10 rounded-xl py-4 pl-12 pr-4 focus:outline-none focus:border-[#07B300]/50 text-base"
            />
          </div>

          <!-- Location Search -->
          <div class="md:w-80 relative group">
            <div
              class="absolute inset-y-0 left-4 flex items-center pointer-events-none"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="20"
                height="20"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="text-gray-500 group-focus-within:text-[#07B300] transition-colors"
              >
                <path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z" />
                <circle cx="12" cy="10" r="3" />
              </svg>
            </div>
            <input
              type="text"
              placeholder="City or location"
              class="w-full bg-[#0A0A0A] border border-white/10 rounded-xl py-4 pl-12 pr-4 focus:outline-none focus:border-[#07B300]/50 text-base"
            />
          </div>

          <!-- Search Button -->
          <button
            class="bg-[#07B300] hover:bg-[#069e00] hover:scale-[1.02] active:scale-[0.98] text-black font-bold px-8 py-4 rounded-xl transition-all flex items-center justify-center gap-2 text-base shadow-[0_0_20px_rgba(7,179,0,0.2)]"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <circle cx="11" cy="11" r="8" />
              <path d="m21 21-4.3-4.3" />
            </svg>
            Search
          </button>
        </div>

        <div class="flex flex-wrap gap-4 items-center">
          <!-- Category Dropdown -->
          <div class="relative min-w-[200px]">
            <button
              @click="isCategoryOpen = !isCategoryOpen"
              class="w-full bg-[#0A0A0A] border border-white/10 rounded-xl py-3 px-4 flex items-center justify-between group hover:border-white/20 transition-all"
            >
              <span class="font-medium">All Categories</span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="20"
                height="20"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                :class="{ 'rotate-180': isCategoryOpen }"
                class="text-gray-500 transition-transform duration-200"
              >
                <path d="m6 9 6 6 6-6" />
              </svg>
            </button>

            <!-- Dropdown Menu -->
            <div
              v-if="isCategoryOpen"
              class="absolute top-full left-0 mt-2 w-full bg-[#0F0F0F] border border-white/10 rounded-xl overflow-hidden z-20 shadow-2xl"
            >
              <div class="max-h-80 overflow-y-auto custom-scrollbar">
                <button
                  v-for="cat in categories"
                  :key="cat"
                  @click="isCategoryOpen = false"
                  class="w-full text-left px-4 py-3 hover:bg-white/5 transition-colors flex items-center justify-between"
                >
                  <span>{{ cat }}</span>
                  <svg
                    v-if="cat === 'All Categories'"
                    xmlns="http://www.w3.org/2000/svg"
                    width="16"
                    height="16"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="#07B300"
                    stroke-width="3"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                  >
                    <path d="M20 6 9 17l-5-5" />
                  </svg>
                </button>
              </div>
            </div>
          </div>

          <!-- More Filters Button -->
          <button
            class="bg-[#0A0A0A] border border-white/10 rounded-xl py-3 px-6 flex items-center gap-2 hover:bg-white/5 transition-all"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="text-gray-400"
            >
              <path d="M21 4H3" />
              <path d="M10 20H3" />
              <path d="M18 12H3" />
              <path d="M21 12h-3" />
              <path d="M14 20h7" />
              <path d="M12 4h9" />
            </svg>
            <span class="font-medium">More Filters</span>
          </button>
        </div>
      </div>

      <!-- Events Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="event in events"
          :key="event.id"
          class="group bg-[#0A0A0A] border border-white/10 rounded-[2rem] overflow-hidden hover:border-[#07B300]/40 transition-all duration-300 flex flex-col h-full"
        >
          <!-- Image Container -->
          <div class="relative aspect-[16/10] overflow-hidden">
            <img
              :src="event.image"
              :alt="event.title"
              @error="handleImageError"
              class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
            />
            <!-- Category Badge -->
            <div class="absolute top-4 left-4">
              <span
                class="bg-[#07B300] text-black text-xs font-bold uppercase tracking-wider px-3 py-1 rounded-md"
              >
                {{ event.category }}
              </span>
            </div>
            <!-- Virtual Badge -->
            <div v-if="event.isVirtual" class="absolute top-4 right-4">
              <span
                class="bg-black/60 backdrop-blur-md text-white text-xs font-bold px-3 py-1 rounded-md"
              >
                Virtual
              </span>
            </div>
            <!-- Date Badge -->
            <div class="absolute bottom-4 left-4">
              <div
                class="bg-black/80 backdrop-blur-md px-3 py-1.5 rounded-lg flex items-center gap-2 border border-white/10"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="14"
                  height="14"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <rect width="18" height="18" x="3" y="4" rx="2" ry="2" />
                  <path d="M16 2v4" />
                  <path d="M8 2v4" />
                  <path d="M3 10h18" />
                </svg>
                <span class="text-sm font-bold text-white">{{
                  event.date
                }}</span>
              </div>
            </div>
          </div>

          <!-- Content -->
          <div class="p-6 flex flex-col flex-grow">
            <h3
              class="text-xl font-bold mb-4 group-hover:text-[#07B300] transition-colors line-clamp-2 min-h-[3.5rem]"
            >
              {{ event.title }}
            </h3>

            <div class="space-y-3 mb-6">
              <div
                class="flex items-start gap-2 text-gray-400 group-hover:text-gray-300 transition-colors"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="mt-1 flex-shrink-0 text-[#07B300]"
                >
                  <path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z" />
                  <circle cx="12" cy="10" r="3" />
                </svg>
                <span class="text-sm line-clamp-1">{{ event.location }}</span>
              </div>
              <div
                class="flex items-center gap-2 text-gray-400 group-hover:text-gray-300 transition-colors"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="flex-shrink-0 text-[#07B300]"
                >
                  <circle cx="12" cy="12" r="10" />
                  <polyline points="12 6 12 12 16 14" />
                </svg>
                <span class="text-sm">{{ event.time }}</span>
                <template v-if="event.spots">
                  <span class="text-gray-600 mx-1">•</span>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="16"
                    height="16"
                    viewBox="0 0 24 24"
                    fill="none"
                    stroke="currentColor"
                    stroke-width="2"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    class="flex-shrink-0 text-[#07B300]"
                  >
                    <path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2" />
                    <circle cx="9" cy="7" r="4" />
                    <path d="M22 21v-2a4 4 0 0 0-3-3.87" />
                    <path d="M16 3.13a4 4 0 0 1 0 7.75" />
                  </svg>
                  <span class="text-sm">{{ event.spots }} spots</span>
                </template>
              </div>
            </div>

            <!-- Footer -->
            <div
              class="mt-auto pt-5 border-t border-white/5 flex items-center justify-between"
            >
              <div class="flex items-center gap-3">
                <div
                  class="w-9 h-9 rounded-full bg-gradient-to-br from-[#07B300] to-[#22c55e] flex items-center justify-center text-black font-bold text-sm shadow-lg"
                >
                  E
                </div>
                <span
                  class="text-sm text-gray-400 group-hover:text-gray-300 font-medium line-clamp-1 transition-colors"
                  >{{ event.organizer }}</span
                >
              </div>
              <button
                class="text-sm font-bold text-gray-500 hover:text-[#07B300] transition-colors flex items-center gap-1 group/btn"
              >
                More
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="14"
                  height="14"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2.5"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="group-hover/btn:translate-x-1 transition-transform"
                >
                  <path d="m9 18 6-6-6-6" />
                </svg>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import eventsData from "~/data/events.json";

const isCategoryOpen = ref(false);
const events = ref(eventsData);

const handleImageError = (event) => {
  event.target.src =
    "https://images.unsplash.com/photo-1501281668745-f7f57925c3b4?q=80&w=2070&auto=format&fit=crop";
};

const categories = [
  "All Categories",
  "Conference",
  "Workshop",
  "Seminar",
  "Concert",
  "Festival",
  "Sports",
  "Networking",
  "Fundraiser",
  "Party",
  "Exhibition",
  "Meetup",
  "Webinar",
  "Class",
  "Retreat",
  "Other",
];
</script>

<style scoped>
.custom-scrollbar::-webkit-scrollbar {
  width: 6px;
}
.custom-scrollbar::-webkit-scrollbar-track {
  background: transparent;
}
.custom-scrollbar::-webkit-scrollbar-thumb {
  background: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
}
.custom-scrollbar::-webkit-scrollbar-thumb:hover {
  background: rgba(255, 255, 255, 0.2);
}
</style>
