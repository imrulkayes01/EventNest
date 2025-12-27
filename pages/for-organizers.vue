<template>
  <div
    class="min-h-screen bg-[#050505] text-white relative flex flex-col items-center justify-center pt-24 pb-20 overflow-hidden font-sans"
  >
    <!-- Content -->
    <section class="relative z-10 max-w-[1280px] mx-auto px-6 text-center">
      <div
        class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full border border-green-500/20 bg-green-500/10 text-green-400 text-sm font-semibold mb-8 animate-fade-in"
      >
        <div class="size-2 rounded-full bg-[#07B300]"></div>
        Built for Organizers
      </div>

      <!-- Headline -->
      <h1
        class="text-5xl md:text-[3.75rem] font-bold tracking-tight mb-8 leading-[1.05] animate-slide-up"
      >
        Everything You Need to <br />
        <span class="text-[#07B300]">Host Successful Events</span>
      </h1>

      <!-- Description -->
      <p
        class="text-gray-400 text-lg md:text-xl max-w-2xl mx-auto mb-12 leading-relaxed animate-slide-up animation-delay-200"
      >
        From planning to execution, EventFlow provides all the tools
        professional organizers need to create memorable experiences and grow
        their audience.
      </p>

      <!-- CTA Buttons -->
      <div
        class="flex flex-col sm:flex-row items-center justify-center gap-4 mb-16 animate-slide-up animation-delay-400"
      >
        <button
          class="bg-[#07B300] hover:bg-[#16a34a] text-black font-bold px-8 py-4 rounded-xl transition-all flex items-center gap-2 text-lg active:scale-95"
        >
          Start Creating Free
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
            <path d="M5 12h14" />
            <path d="m12 5 7 7-7 7" />
          </svg>
        </button>
        <button
          class="bg-transparent border-2 border-white/10 hover:bg-white/5 text-white font-bold px-8 py-4 rounded-xl transition-all flex items-center gap-3 text-lg active:scale-95"
        >
          See How It Works
        </button>
      </div>

      <!-- Feature List -->
      <div
        class="flex flex-wrap justify-center gap-x-10 gap-y-6 text-gray-400 text-sm font-medium animate-fade-in animation-delay-600"
      >
        <div class="flex items-center gap-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="18"
            height="18"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2.5"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="text-[#07B300]"
          >
            <path d="M20 6 9 17l-5-5" />
          </svg>
          Free to start
        </div>
        <div class="flex items-center gap-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="18"
            height="18"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2.5"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="text-[#07B300]"
          >
            <path d="M20 6 9 17l-5-5" />
          </svg>
          No credit card required
        </div>
        <div class="flex items-center gap-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="18"
            height="18"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2.5"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="text-[#07B300]"
          >
            <path d="M20 6 9 17l-5-5" />
          </svg>
          Cancel anytime
        </div>
      </div>
    </section>

    <support-chat />
  </div>
</template>

<script setup></script>

<style scoped>
.animate-fade-in {
  animation: fadeIn 1s ease-out forwards;
}

.animate-slide-up {
  opacity: 0;
  animation: slideUp 0.8s cubic-bezier(0.4, 0, 0.2, 1) forwards;
}

.animation-delay-200 {
  animation-delay: 200ms;
}
.animation-delay-400 {
  animation-delay: 400ms;
}
.animation-delay-600 {
  animation-delay: 600ms;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Custom button transition */
button {
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}
</style>
