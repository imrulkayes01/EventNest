<template>
  <div
    class="min-h-screen bg-black text-white selection:bg-[#22c55e] selection:text-black font-sans"
  >
    <!-- Hero Section -->
    <section
      class="relative flex flex-col items-center justify-center min-h-screen px-4 py-20 overflow-hidden"
    >
      <!-- Green Glow Background Effect -->
      <!-- Content Container -->
      <div
        class="relative z-10 w-full max-w-[1280px] mx-auto text-center flex flex-col items-center"
      >
        <!-- Badge -->
        <span
          class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-[#22c55e]/10 border border-[#22c55e]/20 text-[#22c55e] text-sm font-medium mb-8 animate-fade-in-up"
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
            class="lucide lucide-sparkles"
          >
            <path
              d="m12 3-1.912 5.813a2 2 0 0 1-1.275 1.275L3 12l5.813 1.912a2 2 0 0 1 1.275 1.275L12 21l1.912-5.813a2 2 0 0 1 1.275-1.275L21 12l-5.813-1.912a2 2 0 0 1-1.275-1.275L12 3Z"
            />
          </svg>
          Discover Amazing Events
        </span>

        <!-- Headline -->
        <h1
          class="text-5xl md:text-7xl font-bold tracking-tight mb-6 leading-tight animate-fade-in-up delay-100"
        >
          Create & Experience <br />
          <span class="text-[#22c55e]">Unforgettable Events</span>
        </h1>

        <!-- Subtitle -->
        <p
          class="text-lg md:text-xl text-gray-400 max-w-2xl mb-10 animate-fade-in-up delay-200"
        >
          The all-in-one platform for event organizers and attendees. Create,
          discover, and manage events that leave lasting impressions.
        </p>

        <!-- Search Bar -->
        <div
          class="w-full max-w-3xl bg-white/5 border border-white/10 rounded-2xl p-2 flex flex-col md:flex-row gap-2 backdrop-blur-sm mb-12 animate-fade-in-up delay-300"
        >
          <div
            class="flex-1 flex items-center px-4 h-12 border-b md:border-b-0 md:border-r border-white/10"
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
              class="text-gray-400 mr-3"
            >
              <circle cx="11" cy="11" r="8" />
              <path d="m21 21-4.3-4.3" />
            </svg>
            <input
              type="text"
              placeholder="Search events, concerts, conferences..."
              class="bg-transparent w-full text-white placeholder-gray-500 focus:outline-none"
            />
          </div>
          <div class="flex-1 flex items-center px-4 h-12">
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
              class="text-gray-400 mr-3"
            >
              <path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z" />
              <circle cx="12" cy="10" r="3" />
            </svg>
            <input
              type="text"
              placeholder="Location"
              class="bg-transparent w-full text-white placeholder-gray-500 focus:outline-none"
            />
          </div>
          <button
            class="bg-[#22c55e] hover:bg-[#16a34a] text-black font-semibold px-8 py-3 rounded-[0.50rem] transition-colors h-12 md:h-auto flex items-center justify-center gap-2"
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
            >
              <circle cx="11" cy="11" r="8" />
              <path d="m21 21-4.3-4.3" />
            </svg>
            Search
          </button>
        </div>

        <!-- Action Buttons -->
        <div
          class="flex flex-wrap gap-4 justify-center mb-16 animate-fade-in-up delay-400"
        >
          <button
            class="bg-[#22c55e] hover:bg-[#16a34a] text-black font-semibold px-8 py-3.5 rounded-[0.50rem] transition-all hover:scale-105 flex items-center gap-2"
          >
            Explore Events
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
            >
              <path d="M5 12h14" />
              <path d="m12 5 7 7-7 7" />
            </svg>
          </button>
          <button
            class="bg-transparent border border-white/20 hover:bg-[#22c55e]/20 text-white font-semibold px-8 py-3.5 rounded-[0.50rem] transition-all flex items-center gap-2"
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
            >
              <path
                d="M15 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7Z"
              />
              <path d="M14 2v4a2 2 0 0 0 2 2h4" />
            </svg>
            Create Your Event
          </button>
        </div>

        <!-- Stats -->
        <div
          class="grid grid-cols-2 lg:grid-cols-4 gap-8 md:gap-12 w-full max-w-[1280px] animate-fade-in-up delay-500"
        >
          <div class="text-center">
            <div class="text-3xl md:text-5xl font-bold text-[#22c55e] mb-2">
              10K+
            </div>
            <div class="text-gray-400 text-sm font-medium">Events Hosted</div>
          </div>
          <div class="text-center">
            <div class="text-3xl md:text-5xl font-bold text-[#22c55e] mb-2">
              500K+
            </div>
            <div class="text-gray-400 text-sm font-medium">Tickets Sold</div>
          </div>
          <div class="text-center">
            <div class="text-3xl md:text-5xl font-bold text-[#22c55e] mb-2">
              50K+
            </div>
            <div class="text-gray-400 text-sm font-medium">Organizers</div>
          </div>
          <div class="text-center">
            <div class="text-3xl md:text-5xl font-bold text-[#22c55e] mb-2">
              99.9%
            </div>
            <div class="text-gray-400 text-sm font-medium">Uptime</div>
          </div>
        </div>

        <!-- Scroll Indicator -->
        <div
          class="flex flex-col items-center gap-3 animate-bounce opacity-70 mb-12 mt-12"
        >
          <span class="text-xs text-white/60 font-medium tracking-wide"
            >Scroll to explore</span
          >
          <div
            class="w-6 h-9 border-2 border-white/30 rounded-full flex justify-center p-1"
          >
            <div
              class="w-1.5 h-1.5 bg-[#22c55e] rounded-full animate-scroll-dot"
            ></div>
          </div>
        </div>
      </div>
    </section>

    <!-- Floating Chat Button -->
    <button
      class="fixed bottom-8 right-8 w-14 h-14 bg-[#22c55e] hover:bg-[#16a34a] rounded-full shadow-lg shadow-[#22c55e]/30 flex items-center justify-center text-black transition-transform hover:scale-110 z-50"
    >
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
      >
        <path d="M7.9 20A9 9 0 1 0 4 16.1L2 22Z" />
      </svg>
    </button>
  </div>
</template>

<style>
/* Custom animations if Tailwind config doesn't cover them */
@keyframes scroll-dot {
  0% {
    transform: translateY(0);
    opacity: 1;
  }
  100% {
    transform: translateY(12px);
    opacity: 0;
  }
}
.animate-scroll-dot {
  animation: scroll-dot 1.5s infinite;
}

@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out forwards;
  opacity: 0; /* Star hidden */
}
.delay-100 {
  animation-delay: 0.1s;
}
.delay-200 {
  animation-delay: 0.2s;
}
.delay-300 {
  animation-delay: 0.3s;
}
.delay-400 {
  animation-delay: 0.4s;
}
.delay-500 {
  animation-delay: 0.5s;
}
</style>

<script></script>

<style>
body {
  font-family: "Inter", sans-serif;
}
</style>
