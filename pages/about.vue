<template>
  <div
    class="bg-[#050505] text-white min-h-screen font-sans selection:bg-green-500/30 selection:text-green-400"
  >
    <!-- Hero Section -->
    <section
      class="relative max-w-[1280px] mx-auto pt-44 pb-20 px-6 sm:px-10 lg:px-20 flex flex-col items-center text-center overflow-hidden"
    >
      <!-- Background Glows -->
      <div
        class="absolute top-[-10%] left-1/2 -translate-x-1/2 w-[800px] h-[500px] bg-green-500/5 rounded-full blur-[120px] -z-10"
      ></div>
      <div
        class="absolute bottom-0 left-[-10%] w-[400px] h-[400px] bg-green-500/5 rounded-full blur-[100px] -z-10"
      ></div>

      <div
        class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-green-500/10 border border-green-500/20 text-green-400 text-sm font-semibold mb-8 animate-fade-in"
      >
        <div
          class="w-2 h-2 rounded-full bg-[#07B300] transition-shadow shadow-[#07B300]"
        ></div>
        About EventNest
      </div>

      <h1
        class="text-5xl md:text-6xl font-bold max-w-5xl leading-[1.1] mb-8 tracking-tight"
      >
        Connecting People Through <br class="hidden md:block" />
        <span class="text-[#07B300]">Remarkable Experiences</span>
      </h1>

      <p
        class="text-gray-400 text-lg md:text-xl max-w-3xl mb-12 leading-relaxed"
      >
        We're on a mission to empower event creators worldwide with the tools
        they need to bring people together and create lasting memories.
      </p>

      <div class="flex flex-col sm:flex-row gap-4 items-center justify-center">
        <button
          class="bg-[#07B300] hover:bg-[#16a34a] text-black font-bold px-8 py-4 rounded-xl transition-all flex items-center gap-2 text-lg"
        >
          Start Creating Events
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
            <rect width="18" height="18" x="3" y="4" rx="2" ry="2" />
            <line x1="16" x2="16" y1="2" y2="6" />
            <line x1="8" x2="8" y1="2" y2="6" />
            <line x1="3" x2="21" y1="10" y2="10" />
          </svg>
        </button>
        <button
          class="bg-transparent border-2 border-white/10 hover:bg-white/5 text-white font-bold px-8 py-4 rounded-xl transition-all flex items-center gap-3 text-lg"
        >
          Explore Events
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
      </div>
    </section>

    <!-- Mission & Stats Section -->
    <section
      class="py-24 px-6 sm:px-10 lg:px-20 bg-gradient-to-b from-transparent via-white/[0.01] to-transparent"
    >
      <div
        class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-20 items-center"
      >
        <div class="space-y-6">
          <span
            class="text-[#07B300] font-bold tracking-[0.2em] text-xs uppercase"
            >Our Mission</span
          >
          <h2 class="text-4xl md:text-6xl font-bold leading-tight">
            Making Event Management <br />
            <span class="text-[#07B300]">Simple and Powerful</span>
          </h2>
          <div
            class="space-y-6 text-gray-400 text-lg md:text-xl leading-relaxed"
          >
            <p>
              EventNest was born from a simple observation: event management was
              unnecessarily complex. Organizers spent more time wrestling with
              technology than creating amazing experiences.
            </p>
            <p>
              We set out to change that by building a platform that's powerful
              enough for the world's largest events, yet simple enough for
              first-time organizers to create their dream gathering.
            </p>
          </div>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
          <!-- Stat Cards -->
          <div
            class="p-8 rounded-3xl bg-white/[0.03] border border-white/5 hover:border-green-500/30 transition-all duration-500 group relative overflow-hidden"
          >
            <div
              class="absolute inset-0 bg-gradient-to-br from-green-500/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity"
            ></div>
            <div class="relative z-10">
              <div
                class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10 group-hover:scale-110 transition-transform duration-500"
              >
                <svg
                  class="w-7 h-7 text-green-500"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"
                  />
                </svg>
              </div>
              <div
                class="text-4xl md:text-5xl font-black mb-2 text-white group-hover:text-green-400 transition-colors"
              >
                10K+
              </div>
              <div
                class="text-gray-500 font-medium text-base uppercase tracking-wider"
              >
                Events Created
              </div>
            </div>
          </div>

          <div
            class="p-8 rounded-3xl bg-white/[0.03] border border-white/5 hover:border-green-500/30 transition-all duration-500 group relative overflow-hidden"
          >
            <div
              class="absolute inset-0 bg-gradient-to-br from-green-500/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity"
            ></div>
            <div class="relative z-10">
              <div
                class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10 group-hover:scale-110 transition-transform duration-500"
              >
                <svg
                  class="w-7 h-7 text-green-500"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"
                  />
                </svg>
              </div>
              <div
                class="text-4xl md:text-5xl font-black mb-2 text-white group-hover:text-green-400 transition-colors"
              >
                500K+
              </div>
              <div
                class="text-gray-500 font-medium text-base uppercase tracking-wider"
              >
                Tickets Sold
              </div>
            </div>
          </div>

          <div
            class="p-8 rounded-3xl bg-white/[0.03] border border-white/5 hover:border-green-500/30 transition-all duration-500 group relative overflow-hidden"
          >
            <div
              class="absolute inset-0 bg-gradient-to-br from-green-500/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity"
            ></div>
            <div class="relative z-10">
              <div
                class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10 group-hover:scale-110 transition-transform duration-500"
              >
                <svg
                  class="w-7 h-7 text-green-500"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 002 2h1a2.5 2.5 0 012.5 2.5v.5M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
                  />
                </svg>
              </div>
              <div
                class="text-4xl md:text-5xl font-black mb-2 text-white group-hover:text-green-400 transition-colors"
              >
                50+
              </div>
              <div
                class="text-gray-500 font-medium text-base uppercase tracking-wider"
              >
                Countries
              </div>
            </div>
          </div>

          <div
            class="p-8 rounded-3xl bg-white/[0.03] border border-white/5 hover:border-green-500/30 transition-all duration-500 group relative overflow-hidden"
          >
            <div
              class="absolute inset-0 bg-gradient-to-br from-green-500/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity"
            ></div>
            <div class="relative z-10">
              <div
                class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10 group-hover:scale-110 transition-transform duration-500"
              >
                <svg
                  class="w-7 h-7 text-green-500"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
                  />
                </svg>
              </div>
              <div
                class="text-4xl md:text-5xl font-black mb-2 text-white group-hover:text-green-400 transition-colors"
              >
                99.9%
              </div>
              <div
                class="text-gray-500 font-medium text-base uppercase tracking-wider"
              >
                Uptime
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Values Section -->
    <section class="py-24 px-6 sm:px-10 lg:px-20 bg-[#080808]">
      <div class="max-w-7xl mx-auto text-center mb-20">
        <span
          class="text-[#07B300] font-bold tracking-[0.2em] text-xs uppercase mb-4 block"
          >Our Values</span
        >
        <h2 class="text-4xl md:text-6xl font-bold mb-6">
          What Drives Us <span class="text-[#07B300]">Every Day</span>
        </h2>
        <p class="text-gray-400 text-lg md:text-xl max-w-3xl mx-auto">
          These core values guide every decision we make and shape the platform
          we build.
        </p>
      </div>

      <div
        class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8"
      >
        <!-- Purpose-Driven -->
        <div
          class="group p-10 rounded-3xl bg-white/[0.02] border border-white/5 hover:bg-white/[0.04] transition-all duration-300"
        >
          <div
            class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10"
          >
            <svg
              class="w-7 h-7 text-green-500"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"
              />
            </svg>
          </div>
          <h3
            class="text-2xl font-bold mb-4 group-hover:text-[#07B300] transition-colors"
          >
            Purpose-Driven
          </h3>
          <p class="text-gray-400 text-lg leading-relaxed">
            Every feature we build serves one goal: helping you create better
            events and connect more people.
          </p>
        </div>

        <!-- Community First -->
        <div
          class="group p-10 rounded-3xl bg-white/[0.02] border border-white/5 hover:bg-white/[0.04] transition-all duration-300"
        >
          <div
            class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10"
          >
            <svg
              class="w-7 h-7 text-green-500"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"
              />
            </svg>
          </div>
          <h3
            class="text-2xl font-bold mb-4 group-hover:text-[#07B300] transition-colors"
          >
            Community First
          </h3>
          <p class="text-gray-400 text-lg leading-relaxed">
            We listen to our users, learn from their feedback, and build
            features that solve real problems.
          </p>
        </div>

        <!-- Trust & Security -->
        <div
          class="group p-10 rounded-3xl bg-white/[0.02] border border-white/5 hover:bg-white/[0.04] transition-all duration-300"
        >
          <div
            class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10"
          >
            <svg
              class="w-7 h-7 text-green-500"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
              />
            </svg>
          </div>
          <h3
            class="text-2xl font-bold mb-4 group-hover:text-[#07B300] transition-colors"
          >
            Trust & Security
          </h3>
          <p class="text-gray-400 text-lg leading-relaxed">
            Your data and your attendees' information are protected with
            enterprise-grade security.
          </p>
        </div>

        <!-- Innovation -->
        <div
          class="group p-10 rounded-3xl bg-white/[0.02] border border-white/5 hover:bg-white/[0.04] transition-all duration-300"
        >
          <div
            class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10"
          >
            <svg
              class="w-7 h-7 text-green-500"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M13 10V3L4 14h7v7l9-11h-7z"
              />
            </svg>
          </div>
          <h3
            class="text-2xl font-bold mb-4 group-hover:text-[#07B300] transition-colors"
          >
            Innovation
          </h3>
          <p class="text-gray-400 text-lg leading-relaxed">
            We constantly push boundaries, exploring new technologies to make
            event management better.
          </p>
        </div>

        <!-- Passion -->
        <div
          class="group p-10 rounded-3xl bg-white/[0.02] border border-white/5 hover:bg-white/[0.04] transition-all duration-300"
        >
          <div
            class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10"
          >
            <svg
              class="w-7 h-7 text-green-500"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"
              />
            </svg>
          </div>
          <h3
            class="text-2xl font-bold mb-4 group-hover:text-[#07B300] transition-colors"
          >
            Passion
          </h3>
          <p class="text-gray-400 text-lg leading-relaxed">
            We're event enthusiasts ourselves, and that passion shows in
            everything we create.
          </p>
        </div>

        <!-- Accessibility -->
        <div
          class="group p-10 rounded-3xl bg-white/[0.02] border border-white/5 hover:bg-white/[0.04] transition-all duration-300"
        >
          <div
            class="w-14 h-14 bg-green-500/10 rounded-2xl flex items-center justify-center mb-8 border border-green-500/10"
          >
            <svg
              class="w-7 h-7 text-green-500"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
              />
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M9 10a1 1 0 011-1h4a1 1 0 011 1m-5 4a1 1 0 00-1 1v1a1 1 0 001 1h4a1 1 0 001-1v-1a1 1 0 00-1-1"
              />
            </svg>
          </div>
          <h3
            class="text-2xl font-bold mb-4 group-hover:text-[#07B300] transition-colors"
          >
            Accessibility
          </h3>
          <p class="text-gray-400 text-lg leading-relaxed">
            Great events should be accessible to everyone, everywhere. We build
            with inclusion in mind.
          </p>
        </div>
      </div>
    </section>

    <!-- Story Section -->
    <section class="max-w-7xl mx-auto py-24 px-6 sm:px-10 lg:px-20 text-center">
      <div class="max-w-4xl mx-auto">
        <span
          class="text-[#07B300] font-bold tracking-[0.2em] text-xs uppercase mb-4 block"
          >Our Story</span
        >
        <h2 class="text-4xl md:text-6xl font-bold mb-16">
          From Frustration to <span class="text-[#07B300]">Innovation</span>
        </h2>

        <div
          class="space-y-8 text-gray-400 text-lg md:text-xl leading-relaxed text-left"
        >
          <p>
            EventNest started in 2020 when our founders, both experienced event
            organizers, grew tired of juggling multiple platforms just to run a
            single event. From ticketing to attendee management, from marketing
            to analytics – everything was fragmented.
          </p>
          <p>
            After organizing hundreds of events ranging from intimate workshops
            to conferences with thousands of attendees, they realized there had
            to be a better way. A platform that could handle everything
            seamlessly, without the complexity and sky-high fees of traditional
            solutions.
          </p>
          <p>
            Today, EventNest powers events across 50+ countries, from local
            meetups to international conferences. We've helped organizers sell
            over 500,000 tickets and process millions in revenue – all while
            keeping the platform intuitive and affordable.
          </p>
          <p>
            But we're just getting started. Our roadmap is packed with features
            that will make event management even more powerful, and we're
            excited to build them with feedback from our amazing community of
            organizers.
          </p>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section
      class="max-w-7xl mx-auto py-24 px-6 sm:px-10 lg:px-20 text-center relative overflow-hidden"
    >
      <div
        class="absolute bottom-[-20%] left-1/2 -translate-x-1/2 w-[1000px] h-[400px] bg-green-500/10 rounded-full blur-[150px] -z-10"
      ></div>

      <div
        class="max-w-4xl mx-auto px-6 py-20 rounded-[40px] bg-gradient-to-b from-white/[0.04] to-transparent border border-white/10"
      >
        <h2 class="text-4xl md:text-6xl font-bold mb-8">
          Ready to Create Your <br />
          <span class="text-[#07B300] italic">Next Event?</span>
        </h2>
        <p
          class="text-gray-400 text-xl md:text-2xl mb-12 max-w-2xl mx-auto leading-relaxed font-sm"
        >
          Join thousands of organizers who trust EventNest to power their
          events. Start free, scale as you grow.
        </p>

        <div
          class="flex flex-col sm:flex-row gap-6 justify-center items-center"
        >
          <button
            class="bg-[#07B300] hover:bg-[#16a34a] text-black font-bold px-12 py-5 rounded-2xl transition-all flex items-center gap-2 text-lg"
          >
            Get Started Free
          </button>
          <button
            class="bg-transparent border-2 border-white/10 hover:bg-white/5 text-white font-bold px-12 py-5 rounded-2xl transition-all flex items-center gap-3 text-lg"
          >
            Learn More
          </button>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
useHead({
  title: "About Us | EventNest",
  meta: [
    {
      name: "description",
      content:
        "Discover the story behind EventNest, our mission to simplify event management, and the core values that drive our innovation.",
    },
  ],
});
</script>

<style scoped>
@keyframes fade-in {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in {
  animation: fade-in 1s ease-out forwards;
}

/* Custom scrollbar */
::-webkit-scrollbar {
  width: 8px;
}
::-webkit-scrollbar-track {
  background: #050505;
}
::-webkit-scrollbar-thumb {
  background: #22c55e;
  border-radius: 4px;
}
::-webkit-scrollbar-thumb:hover {
  background: #16a34a;
}
</style>
