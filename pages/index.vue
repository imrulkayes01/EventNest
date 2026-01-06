<template>
  <div
    class="min-h-screen bg-black text-white selection:bg-[#22c55e] selection:text-black font-sans"
  >
    <!-- Hero Section -->
    <section
      class="relative flex flex-col items-center justify-center min-h-screen px-4 py-24 overflow-hidden"
    >
      <div
        class="relative z-10 w-full max-w-[1280px] mx-auto text-center flex flex-col items-center"
      >
        <!-- Badge -->
        <span
          class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-[#22c55e]/10 border border-[#22c55e]/20 text-[#07B300] text-sm font-medium mb-8 animate-fade-in-up"
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
          class="text-5xl md:text-8xl font-bold tracking-tight mb-6 leading-tight animate-fade-in-up delay-100"
        >
          Create & Experience <br />
          <span class="text-[#07B300]">Unforgettable Events</span>
        </h1>

        <!-- Subtitle -->
        <p
          class="text-xl md:text-xl text-gray-400 max-w-2xl mb-10 animate-fade-in-up delay-200"
        >
          The all-in-one platform for event organizers and attendees. Create,
          discover, and manage events that leave lasting impressions.
        </p>

        <!-- Search Bar -->
        <div
          class="w-full max-w-3xl bg-[#0A0A0A] border border-white/10 rounded-2xl p-2 flex flex-col md:flex-row gap-2 backdrop-blur-sm mb-12 animate-fade-in-up delay-300"
        >
          <div
            class="flex-1 flex items-center px-4 h-14 border-b md:border-b-0 md:border-r border-white/10"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="22"
              height="22"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="text-white/40 mr-3"
            >
              <circle cx="11" cy="11" r="8" />
              <path d="m21 21-4.3-4.3" />
            </svg>
            <input
              v-model="searchQuery"
              type="text"
              placeholder="Search events, concerts, conferences..."
              class="bg-transparent w-full text-white placeholder-white/30 focus:outline-none font-medium"
              @keyup.enter="handleSearch"
            />
          </div>
          <div class="flex-1 flex items-center px-4 h-14">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="22"
              height="22"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="text-white/40 mr-3"
            >
              <path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z" />
              <circle cx="12" cy="10" r="3" />
            </svg>
            <input
              v-model="searchLocation"
              type="text"
              placeholder="Location"
              class="bg-transparent w-full text-white placeholder-white/30 focus:outline-none font-medium"
              @keyup.enter="handleSearch"
            />
          </div>
          <button
            @click="handleSearch"
            class="bg-[#07B300] hover:bg-[#16a34a] text-black font-bold px-8 py-3 rounded-xl transition-colors h-14 md:h-auto flex items-center justify-center gap-2"
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

        <!-- Action Buttons -->
        <div
          class="flex flex-wrap gap-4 justify-center mb-16 animate-fade-in-up delay-400"
        >
          <NuxtLink
            to="/discover"
            class="bg-[#07B300] hover:bg-[#16a34a] text-black font-bold px-8 py-4 rounded-xl transition-all hover:scale-105 flex items-center gap-2 text-lg"
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
          </NuxtLink>
          <NuxtLink
            to="/for-organizers"
            class="bg-transparent border-2 border-white/10 hover:bg-white/5 text-white font-bold px-8 py-4 rounded-xl transition-all flex items-center gap-3 text-lg"
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
              <rect width="18" height="18" x="3" y="4" rx="2" ry="2" />
              <line x1="16" x2="16" y1="2" y2="6" />
              <line x1="8" x2="8" y1="2" y2="6" />
              <line x1="3" x2="21" y1="10" y2="10" />
            </svg>
            Create Your Event
          </NuxtLink>
        </div>

        <!-- Stats -->
        <div
          class="grid grid-cols-2 md:grid-cols-4 gap-6 md:gap-8 lg:gap-12 w-full animate-fade-in-up delay-500"
        >
          <div class="text-center">
            <div
              class="text-3xl md:text-4xl lg:text-5xl font-bold text-[#07B300] mb-2"
            >
              <count-up end="10" suffix="K+" />
            </div>
            <div class="text-gray-400 text-sm font-medium">Events Hosted</div>
          </div>
          <div class="text-center">
            <div
              class="text-3xl md:text-4xl lg:text-5xl font-bold text-[#07B300] mb-2"
            >
              <count-up end="500" suffix="K+" />
            </div>
            <div class="text-gray-400 text-sm font-medium">Tickets Sold</div>
          </div>
          <div class="text-center">
            <div
              class="text-3xl md:text-4xl lg:text-5xl font-bold text-[#07B300] mb-2"
            >
              <count-up end="50" suffix="K+" />
            </div>
            <div class="text-gray-400 text-sm font-medium">Organizers</div>
          </div>
          <div class="text-center">
            <div
              class="text-3xl md:text-4xl lg:text-5xl font-bold text-[#07B300] mb-2"
            >
              <count-up end="99.9" suffix="%" :decimals="1" />
            </div>
            <div class="text-gray-400 text-sm font-medium">Uptime</div>
          </div>
        </div>
      </div>

      <!-- Scroll Indicator -->
      <div
        class="absolute bottom-24 flex flex-col items-center gap-3 animate-bounce cursor-pointer"
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
    </section>

    <!-- Features Section -->
    <section class="py-24 bg-[#0A0A0A] relative" id="features">
      <div
        class="w-full max-w-[1280px] mx-auto px-4 text-center flex flex-col items-center"
      >
        <span
          class="text-[#07B300] font-semibold tracking-wider text-sm uppercase mb-4"
        >
          Features
        </span>
        <h2
          class="text-3xl md:text-6xl font-bold text-white mb-6 leading-tight"
        >
          Everything You Need to <br />
          <span class="text-[#07B300]">Run Successful Events</span>
        </h2>
        <p class="text-gray-400 text-xl max-w-2xl mb-16">
          From planning to execution, our platform provides all the tools you
          need to create memorable experiences.
        </p>

        <div
          class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 w-full text-left"
        >
          <!-- Card 1: Event Creation (Highlighted) -->
          <div
            class="group p-8 rounded-2xl bg-black border border-[#22c55e] hover:bg-[#22c55e]/5 transition-all duration-300"
          >
            <div
              class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
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
                class="text-[#22c55e]"
              >
                <rect width="18" height="18" x="3" y="4" rx="2" ry="2" />
                <line x1="16" x2="16" y1="2" y2="6" />
                <line x1="8" x2="8" y1="2" y2="6" />
                <line x1="3" x2="21" y1="10" y2="10" />
              </svg>
            </div>
            <h3 class="text-xl font-bold text-[#22c55e] mb-3">
              Event Creation
            </h3>
            <p class="text-gray-400 text-lg leading-relaxed">
              Create stunning events in minutes with our intuitive builder. Add
              all details, from venue to ticketing.
            </p>
          </div>

          <!-- Card 2: Smart Ticketing -->
          <div
            class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 hover:bg-[#22c55e]/5 transition-all duration-300"
          >
            <div
              class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
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
                class="text-[#22c55e]"
              >
                <path
                  d="M2 9a3 3 0 0 1 0 6v2a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2v-2a3 3 0 0 1 0-6V7a2 2 0 0 0-2-2H4a2 2 0 0 0-2 2Z"
                />
                <path d="M13 5v2" />
                <path d="M13 17v2" />
                <path d="M13 11v2" />
              </svg>
            </div>
            <h3
              class="text-xl font-bold text-white group-hover:text-[#07B300] transition-colors mb-3"
            >
              Smart Ticketing
            </h3>
            <p class="text-gray-400 text-lg leading-relaxed">
              Flexible ticket types, dynamic pricing, and QR code validation for
              seamless check-ins and smooth user experience
            </p>
          </div>

          <!-- Card 3: Secure Payments -->
          <div
            class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 hover:bg-[#22c55e]/5 transition-all duration-300"
          >
            <div
              class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
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
                class="text-[#22c55e]"
              >
                <rect width="20" height="14" x="2" y="5" rx="2" />
                <line x1="2" x2="22" y1="10" y2="10" />
              </svg>
            </div>
            <h3
              class="text-xl font-bold text-white group-hover:text-[#07B300] transition-colors mb-3"
            >
              Secure Payments
            </h3>
            <p class="text-gray-400 text-lg leading-relaxed">
              Accept payments globally with Stripe integration. Multiple
              currencies and payment methods.
            </p>
          </div>

          <!-- Card 4: Real-time Analytics -->
          <div
            class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 hover:bg-[#22c55e]/5 transition-all duration-300"
          >
            <div
              class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
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
                class="text-[#22c55e]"
              >
                <path d="M3 3v18h18" />
                <path d="m18 9-5 5-4-4-3 3" />
              </svg>
            </div>
            <h3
              class="text-xl font-bold text-white group-hover:text-[#07B300] transition-colors mb-3"
            >
              Real-time Analytics
            </h3>
            <p class="text-gray-400 text-lg leading-relaxed">
              Track sales, attendance, and revenue with comprehensive dashboards
              and reports.
            </p>
          </div>

          <!-- Card 5: Attendee Management -->
          <div
            class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 hover:bg-[#22c55e]/5 transition-all duration-300"
          >
            <div
              class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
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
                class="text-[#22c55e]"
              >
                <path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2" />
                <circle cx="9" cy="7" r="4" />
                <path d="M22 21v-2a4 4 0 0 0-3-3.87" />
                <path d="M16 3.13a4 4 0 0 1 0 7.75" />
              </svg>
            </div>
            <h3
              class="text-xl font-bold text-white group-hover:text-[#07B300] transition-colors mb-3"
            >
              Attendee Management
            </h3>
            <p class="text-gray-400 text-lg leading-relaxed">
              Manage guest lists, send notifications, and handle waitlists
              effortlessly.
            </p>
          </div>

          <!-- Card 6: Fraud Protection -->
          <div
            class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 hover:bg-[#22c55e]/5 transition-all duration-300"
          >
            <div
              class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
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
                class="text-[#22c55e]"
              >
                <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z" />
              </svg>
            </div>
            <h3
              class="text-xl font-bold text-white group-hover:text-[#07B300] transition-colors mb-3"
            >
              Fraud Protection
            </h3>
            <p class="text-gray-400 text-lg leading-relaxed">
              Advanced security measures to prevent ticket fraud and
              unauthorized access.
            </p>
          </div>

          <!-- Card 7: Instant Check-in -->
          <div
            class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 hover:bg-[#22c55e]/5 transition-all duration-300"
          >
            <div
              class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
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
                class="text-[#22c55e]"
              >
                <polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2" />
              </svg>
            </div>
            <h3
              class="text-xl font-bold text-white group-hover:text-[#07B300] transition-colors mb-3"
            >
              Instant Check-in
            </h3>
            <p class="text-gray-400 text-lg leading-relaxed">
              Scan tickets with any device. Fast, reliable, and works offline.
            </p>
          </div>

          <!-- Card 8: Virtual Events -->
          <div
            class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 hover:bg-[#22c55e]/5 transition-all duration-300"
          >
            <div
              class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
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
                class="text-[#22c55e]"
              >
                <circle cx="12" cy="12" r="10" />
                <line x1="2" x2="22" y1="12" y2="12" />
                <path
                  d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"
                />
              </svg>
            </div>
            <h3
              class="text-xl font-bold text-white group-hover:text-[#07B300] transition-colors mb-3"
            >
              Virtual Events
            </h3>
            <p class="text-gray-400 text-lg leading-relaxed">
              Host hybrid or fully virtual events with integrated streaming
              platforms.
            </p>
          </div>

          <!-- Card 9: Smart Notifications -->
          <div
            class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 hover:bg-[#22c55e]/5 transition-all duration-300"
          >
            <div
              class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform"
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
                class="text-[#22c55e]"
              >
                <path d="M6 8a6 6 0 0 1 12 0c0 7 3 9 3 9H3s3-2 3-9" />
                <path d="M10.3 21a1.94 1.94 0 0 0 3.4 0" />
              </svg>
            </div>
            <h3
              class="text-xl font-bold text-white group-hover:text-[#07B300] transition-colors mb-3"
            >
              Smart Notifications
            </h3>
            <p class="text-gray-400 text-lg leading-relaxed">
              Automated reminders and updates via email, SMS, and push
              notifications.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Platform Statistics Section -->
    <section class="py-24 bg-black relative">
      <div class="w-full max-w-[1280px] mx-auto px-4">
        <div class="text-center mb-16 flex flex-col items-center">
          <span
            class="text-[#07B300] font-semibold tracking-wider text-sm uppercase mb-4"
          >
            Platform Statistics
          </span>
          <h2
            class="text-3xl md:text-6xl font-bold text-white mb-6 leading-tight"
          >
            Trusted by <br class="hidden md:block" />
            <span class="text-[#07B300]">Thousands Worldwide</span>
          </h2>
          <p class="text-gray-400 text-xl max-w-2xl">
            Real-time metrics that showcase the scale and reliability of our
            event management platform.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-16">
          <!-- Stat Card 1 -->
          <div
            class="p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 transition-all duration-300 group"
          >
            <div class="flex justify-between items-start mb-6">
              <div
                class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center text-[#22c55e]"
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
                >
                  <rect width="18" height="18" x="3" y="4" rx="2" ry="2" />
                  <line x1="16" x2="16" y1="2" y2="6" />
                  <line x1="8" x2="8" y1="2" y2="6" />
                  <line x1="3" x2="21" y1="10" y2="10" />
                </svg>
              </div>
              <svg
                width="60"
                height="30"
                viewBox="0 0 60 30"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="text-[#07B300]"
              >
                <path
                  d="M1 25C10 22 15 28 25 15C35 2 45 18 59 1"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                />
              </svg>
            </div>
            <div class="text-4xl font-bold text-[#07B300] mb-2">
              <count-up end="25000" suffix="+" />
            </div>
            <div class="text-xl font-bold text-white mb-2">Events Created</div>
            <div class="text-gray-400 text-base">
              Successfully hosted events
            </div>
          </div>

          <!-- Stat Card 2 -->
          <div
            class="p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#07B300]/50 transition-all duration-300 group"
          >
            <div class="flex justify-between items-start mb-6">
              <div
                class="w-12 h-12 rounded-lg bg-[#07B300]/10 flex items-center justify-center text-[#07B300]"
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
                >
                  <path
                    d="M2 9a3 3 0 0 1 0 6v2a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2v-2a3 3 0 0 1 0-6V7a2 2 0 0 0-2-2H4a2 2 0 0 0-2 2Z"
                  />
                  <path d="M13 5v2" />
                  <path d="M13 17v2" />
                  <path d="M13 11v2" />
                </svg>
              </div>
              <svg
                width="60"
                height="30"
                viewBox="0 0 60 30"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="text-[#07B300]"
              >
                <path
                  d="M1 28C15 25 20 15 30 18C40 21 50 10 59 5"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                />
              </svg>
            </div>
            <div class="text-4xl font-bold text-[#07B300] mb-2">
              <count-up end="2" suffix="M+" />
            </div>
            <div class="text-xl font-bold text-white mb-2">Tickets Sold</div>
            <div class="text-gray-400 text-base">Across all event types</div>
          </div>

          <!-- Stat Card 3 -->
          <div
            class="p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 transition-all duration-300 group"
          >
            <div class="flex justify-between items-start mb-6">
              <div
                class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center text-[#22c55e]"
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
                >
                  <path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2" />
                  <circle cx="9" cy="7" r="4" />
                  <path d="M22 21v-2a4 4 0 0 0-3-3.87" />
                  <path d="M16 3.13a4 4 0 0 1 0 7.75" />
                </svg>
              </div>
              <svg
                width="60"
                height="30"
                viewBox="0 0 60 30"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="text-[#22c55e]"
              >
                <path
                  d="M1 22C10 20 20 25 30 15C40 5 50 10 59 2"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                />
              </svg>
            </div>
            <div class="text-4xl font-bold text-[#22c55e] mb-2">
              <count-up end="150000" suffix="+" />
            </div>
            <div class="text-xl font-bold text-white mb-2">Active Users</div>
            <div class="text-gray-400 text-base">Organizers & attendees</div>
          </div>

          <!-- Stat Card 4 -->
          <div
            class="p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#22c55e]/50 transition-all duration-300 group"
          >
            <div class="flex justify-between items-start mb-6">
              <div
                class="w-12 h-12 rounded-lg bg-[#22c55e]/10 flex items-center justify-center text-[#22c55e]"
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
                >
                  <line x1="12" x2="12" y1="2" y2="22" />
                  <path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6" />
                </svg>
              </div>
              <svg
                width="60"
                height="30"
                viewBox="0 0 60 30"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="text-[#07B300]"
              >
                <path
                  d="M1 20C10 25 20 15 30 20C40 25 50 5 59 10"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                />
              </svg>
            </div>
            <div class="text-4xl font-bold text-[#07B300] mb-2">
              <count-up end="50" suffix="M+" />
            </div>
            <div class="text-xl font-bold text-white mb-2">
              Revenue Processed
            </div>
            <div class="text-gray-400 text-base">Secure transactions</div>
          </div>

          <!-- Stat Card 5 -->
          <div
            class="p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#07B300]/50 transition-all duration-300 group"
          >
            <div class="flex justify-between items-start mb-6">
              <div
                class="w-12 h-12 rounded-lg bg-[#07B300]/10 flex items-center justify-center text-[#07B300]"
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
                >
                  <circle cx="12" cy="12" r="10" />
                  <line x1="2" x2="22" y1="12" y2="12" />
                  <path
                    d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1 4-10z"
                  />
                </svg>
              </div>
              <svg
                width="60"
                height="30"
                viewBox="0 0 60 30"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="text-[#07B300]"
              >
                <path
                  d="M1 25C10 15 20 20 30 10C40 5 50 15 59 5"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                />
              </svg>
            </div>
            <div class="text-4xl font-bold text-[#07B300] mb-2">
              <count-up end="120" suffix="+" />
            </div>
            <div class="text-xl font-bold text-white mb-2">Countries</div>
            <div class="text-gray-400 text-base">Global reach</div>
          </div>

          <!-- Stat Card 6 -->
          <div
            class="p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#07B300]/50 transition-all duration-300 group"
          >
            <div class="flex justify-between items-start mb-6">
              <div
                class="w-12 h-12 rounded-lg bg-[#07B300]/10 flex items-center justify-center text-[#07B300]"
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
                >
                  <polyline points="22 7 13.5 15.5 8.5 10.5 2 17" />
                  <polyline points="16 7 22 7 22 13" />
                </svg>
              </div>
              <svg
                width="60"
                height="30"
                viewBox="0 0 60 30"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="text-[#07B300]"
              >
                <path
                  d="M1 28C10 20 20 25 30 15C40 10 50 15 59 5"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                />
              </svg>
            </div>
            <div class="text-4xl font-bold text-[#07B300] mb-2">
              <count-up end="99.0" suffix="%" :decimals="1" />
            </div>
            <div class="text-xl font-bold text-white mb-2">Uptime</div>
            <div class="text-gray-400 text-base">Reliable platform</div>
          </div>
        </div>

        <!-- Live Data Indicator -->
        <div class="flex items-center justify-center gap-2">
          <span class="relative flex h-3 w-3">
            <span
              class="animate-ping absolute inline-flex h-full w-full rounded-full bg-[#07B300] opacity-75"
            ></span>
            <span
              class="relative inline-flex rounded-full h-3 w-3 bg-[#07B300]"
            ></span>
          </span>
          <span class="text-gray-400 text-base">
            Live data - Updated in real-time
          </span>
        </div>
      </div>
    </section>

    <!-- How It Works Section -->
    <section
      class="py-24 bg-[#0A0A0A] relative overflow-hidden"
      id="how-it-works"
    >
      <div
        class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[800px] h-[800px] bg-[#22c55e]/5 rounded-full blur-[120px] pointer-events-none"
      ></div>

      <div class="w-full max-w-[1280px] mx-auto px-4 relative z-10">
        <div class="text-center mb-20 flex flex-col items-center">
          <span
            class="text-[#07B300] font-semibold tracking-wider text-sm uppercase mb-4"
          >
            How It Works
          </span>
          <h2
            class="text-3xl md:text-6xl font-bold text-white mb-6 leading-tight"
          >
            Launch Your Event <br class="hidden md:block" />
            <span class="text-[#07B300]">in Four Simple Steps</span>
          </h2>
          <p class="text-gray-400 text-xl max-w-2xl">
            Our streamlined process makes it easy to go from idea to sold-out
            event.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 lg:gap-12">
          <!-- Step 1 -->
          <div class="relative group">
            <div
              class="absolute -top-2 -left-2 md:-left-4 w-8 h-8 md:w-12 md:h-12 bg-[#07B300] text-black font-bold text-base md:text-xl rounded-full flex items-center justify-center z-20 shadow-lg shadow-[#22c55e]/20"
            >
              01
            </div>
            <div
              class="bg-black border border-white/10 rounded-3xl p-8 md:p-10 hover:border-[#22c55e]/30 transition-all duration-300 h-full"
            >
              <h3 class="text-2xl font-bold text-white mb-4 mt-2">
                Create Your Event
              </h3>
              <p class="text-gray-400 text-lg mb-8 leading-relaxed">
                Set up your event in minutes. Add details, upload images, and
                configure ticket types.
              </p>
              <ul class="space-y-4">
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Drag-and-drop builder
                </li>
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Custom branding
                </li>
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Multiple ticket tiers
                </li>
              </ul>
            </div>
          </div>

          <!-- Step 2 -->
          <div class="relative group">
            <div
              class="absolute -top-2 -left-2 md:-left-4 w-8 h-8 md:w-12 md:h-12 bg-[#07B300] text-black font-bold text-base md:text-xl rounded-full flex items-center justify-center z-20 shadow-lg shadow-[#22c55e]/20"
            >
              02
            </div>
            <div
              class="bg-black border border-white/10 rounded-3xl p-8 md:p-10 hover:border-[#22c55e]/30 transition-all duration-300 h-full"
            >
              <h3 class="text-2xl font-bold text-white mb-4 mt-2">
                Publish & Promote
              </h3>
              <p class="text-gray-400 text-lg mb-8 leading-relaxed">
                Share your event with the world. Get discovered by thousands of
                potential attendees.
              </p>
              <ul class="space-y-4">
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  SEO optimization
                </li>
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Social sharing
                </li>
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Email campaigns
                </li>
              </ul>
            </div>
          </div>

          <!-- Step 3 -->
          <div class="relative group">
            <div
              class="absolute -top-2 -left-2 md:-left-4 w-8 h-8 md:w-12 md:h-12 bg-[#07B300] text-black font-bold text-base md:text-xl rounded-full flex items-center justify-center z-20 shadow-lg shadow-[#22c55e]/20"
            >
              03
            </div>
            <div
              class="bg-black border border-white/10 rounded-3xl p-8 md:p-10 hover:border-[#22c55e]/30 transition-all duration-300 h-full"
            >
              <h3 class="text-2xl font-bold text-white mb-4 mt-2">
                Sell Tickets
              </h3>
              <p class="text-gray-400 text-lg mb-8 leading-relaxed">
                Accept secure payments and manage sales in real-time with our
                powerful dashboard.
              </p>
              <ul class="space-y-4">
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Multiple currencies
                </li>
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Promo codes
                </li>
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Waitlist management
                </li>
              </ul>
            </div>
          </div>

          <!-- Step 4 -->
          <div class="relative group">
            <div
              class="absolute -top-2 -left-2 md:-left-4 w-8 h-8 md:w-12 md:h-12 bg-[#07B300] text-black font-bold text-base md:text-xl rounded-full flex items-center justify-center z-20 shadow-lg shadow-[#22c55e]/20"
            >
              04
            </div>
            <div
              class="bg-black border border-white/10 rounded-3xl p-8 md:p-10 hover:border-[#22c55e]/30 transition-all duration-300 h-full"
            >
              <h3 class="text-2xl font-bold text-white mb-4 mt-2">
                Check-in Attendees
              </h3>
              <p class="text-gray-400 text-lg mb-8 leading-relaxed">
                Seamless check-in with QR scanning. Track attendance and manage
                entry in real-time.
              </p>
              <ul class="space-y-4">
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  QR code scanning
                </li>
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Offline mode
                </li>
                <li class="flex items-center text-gray-300">
                  <div
                    class="w-6 h-6 rounded-full bg-[#22c55e]/10 flex items-center justify-center mr-3 text-[#22c55e]"
                  >
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      width="14"
                      height="14"
                      viewBox="0 0 24 24"
                      fill="none"
                      stroke="currentColor"
                      stroke-width="3"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                    >
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  Live attendance stats
                </li>
              </ul>
            </div>
          </div>
        </div>

        <!-- CTA Button -->
        <div class="mt-16 text-center">
          <button
            class="bg-[#00D100] hover:bg-[#00b300] text-black font-bold text-lg px-8 py-4 rounded-lg transition-all hover:scale-105 flex items-center gap-2 mx-auto"
          >
            Start Creating Events
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
            >
              <path d="M5 12h14" />
              <path d="m12 5 7 7-7 7" />
            </svg>
          </button>
        </div>
      </div>
    </section>

    <!-- Integrations Section -->
    <section class="py-24 bg-black relative">
      <div class="w-full max-w-[1280px] mx-auto px-4">
        <div class="text-center mb-16 flex flex-col items-center">
          <span
            class="text-[#07B300] font-semibold tracking-wider text-sm uppercase mb-4"
          >
            Integrations
          </span>
          <h2
            class="text-3xl md:text-6xl font-bold text-white mb-6 leading-tight"
          >
            Connect Your <span class="text-[#07B300]">Favorite Tools</span>
          </h2>
          <p class="text-gray-400 text-xl max-w-2xl">
            EventNest seamlessly integrates with the tools you already use,
            creating a unified event management experience.
          </p>
        </div>

        <div class="grid lg:grid-cols-2 gap-12 items-start mb-20 items-center">
          <!-- Left: List of Integrations -->
          <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div
              v-for="(item, index) in integrations"
              :key="item.id"
              @click="selectedIntegrationIndex = index"
              :class="[
                'p-6 rounded-xl cursor-pointer transition-all duration-300 border flex flex-col items-start gap-4',
                selectedIntegrationIndex === index
                  ? 'bg-black border-[#07B300] shadow-[0_0_20px_-5px_rgba(7,179,0,0.3)]'
                  : 'bg-[#0A0A0A] border-white/5 hover:bg-[#22c55e]/5 hover:border-[#22c55e]/30 group',
              ]"
            >
              <div
                :class="[
                  'w-10 h-10 rounded-lg flex items-center justify-center transition-colors',
                  selectedIntegrationIndex === index
                    ? 'bg-[#07B300]/10 text-[#07B300]'
                    : 'bg-white/5 text-gray-400 group-hover:text-[#22c55e] group-hover:bg-[#22c55e]/10',
                ]"
              >
                <!-- Icon mapping -->
                <svg
                  v-if="item.icon === 'payment'"
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
                  <rect width="20" height="14" x="2" y="5" rx="2" />
                  <line x1="2" x2="22" y1="10" y2="10" />
                </svg>
                <svg
                  v-if="item.icon === 'analytics'"
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
                  <line x1="18" x2="18" y1="20" y2="10" />
                  <line x1="12" x2="12" y1="20" y2="4" />
                  <line x1="6" x2="6" y1="20" y2="14" />
                </svg>
                <svg
                  v-if="item.icon === 'email'"
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
                  <rect width="20" height="16" x="2" y="4" rx="2" />
                  <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7" />
                </svg>
                <svg
                  v-if="item.icon === 'calendar'"
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
                  <rect width="18" height="18" x="3" y="4" rx="2" ry="2" />
                  <line x1="16" x2="16" y1="2" y2="6" />
                  <line x1="8" x2="8" y1="2" y2="6" />
                  <line x1="3" x2="21" y1="10" y2="10" />
                </svg>
                <svg
                  v-if="item.icon === 'messaging'"
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
                    d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"
                  />
                </svg>
                <svg
                  v-if="item.icon === 'streaming'"
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
                  <path d="m22 2-7 20-4-9-9-4Z" />
                  <path d="M22 2 11 13" />
                </svg>
              </div>
              <h3
                :class="[
                  'font-semibold text-base transition-colors',
                  selectedIntegrationIndex === index
                    ? 'text-[#07B300]'
                    : 'text-gray-400 group-hover:text-white',
                ]"
              >
                {{ item.name }}
              </h3>
            </div>
          </div>

          <!-- Right: Details Panel -->
          <div
            class="bg-[#0A0A0A] border border-white/10 rounded-2xl p-8 lg:p-10 relative overflow-hidden min-h-[480px] flex flex-col"
          >
            <!-- Background Glow -->
            <div
              class="absolute top-0 right-0 w-64 h-64 bg-[#07B300]/10 rounded-full blur-[80px] -translate-y-1/2 translate-x-1/2"
            ></div>

            <div class="relative z-10 flex-1">
              <div class="flex items-center gap-4 mb-8">
                <div
                  class="w-14 h-14 rounded-xl bg-[#07B300]/10 flex items-center justify-center text-[#07B300] border border-[#07B300]/20"
                >
                  <!-- Large Icon -->
                  <svg
                    v-if="selectedIntegration.icon === 'payment'"
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
                    <rect width="20" height="14" x="2" y="5" rx="2" />
                    <line x1="2" x2="22" y1="10" y2="10" />
                  </svg>
                  <svg
                    v-if="selectedIntegration.icon === 'analytics'"
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
                    <line x1="18" x2="18" y1="20" y2="10" />
                    <line x1="12" x2="12" y1="20" y2="4" />
                    <line x1="6" x2="6" y1="20" y2="14" />
                  </svg>
                  <svg
                    v-if="selectedIntegration.icon === 'email'"
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
                    <rect width="20" height="16" x="2" y="4" rx="2" />
                    <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7" />
                  </svg>
                  <svg
                    v-if="selectedIntegration.icon === 'calendar'"
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
                    <rect width="18" height="18" x="3" y="4" rx="2" ry="2" />
                    <line x1="16" x2="16" y1="2" y2="6" />
                    <line x1="8" x2="8" y1="2" y2="6" />
                    <line x1="3" x2="21" y1="10" y2="10" />
                  </svg>
                  <svg
                    v-if="selectedIntegration.icon === 'messaging'"
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
                    <path
                      d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"
                    />
                  </svg>
                  <svg
                    v-if="selectedIntegration.icon === 'streaming'"
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
                    <path d="m22 2-7 20-4-9-9-4Z" />
                    <path d="M22 2 11 13" />
                  </svg>
                </div>
                <div>
                  <h3 class="text-2xl font-bold text-white">
                    {{ selectedIntegration.name }}
                  </h3>
                  <p class="text-gray-400 text-lg">
                    {{ selectedIntegration.description }}
                  </p>
                </div>
              </div>

              <!-- Feature List -->
              <div class="space-y-4 mb-10 transition-all duration-300">
                <div
                  v-for="(feature, fIndex) in selectedIntegration.features"
                  :key="fIndex"
                  class="flex items-center gap-3 bg-black/50 p-4 rounded-xl border border-white/5 animate-fade-in"
                  :style="{ animationDelay: fIndex * 100 + 'ms' }"
                >
                  <div class="text-[#07B300]">
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
                      class="text-[#07B300]"
                    >
                      <path
                        d="M11 2a2 2 0 0 0-2 2v5H4a2 2 0 0 0-2 2v2c0 1.1.9 2 2 2h5v5c0 1.1.9 2 2 2h2a2 2 0 0 0 2-2v-5h5a2 2 0 0 0 2-2v-2a2 2 0 0 0-2-2h-5V4a2 2 0 0 0-2-2h-2z"
                        v-if="false"
                      />
                      <polyline points="20 6 9 17 4 12" />
                    </svg>
                  </div>
                  <span class="text-white text-lg">{{ feature }}</span>
                </div>
              </div>
            </div>

            <!-- Action Button -->
            <button
              class="w-full py-4 rounded-xl bg-[#07B300] hover:bg-[#16a34a] text-black font-bold flex items-center justify-center gap-2 transition-all group overflow-hidden relative"
            >
              <span class="relative z-10">Explore All Integrations</span>
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
                class="relative z-10 group-hover:translate-x-1 transition-transform"
              >
                <line x1="5" y1="12" x2="19" y2="12" />
                <polyline points="12 5 19 12 12 19" />
              </svg>
            </button>
          </div>
        </div>

        <!-- Bottom Stats -->
        <div
          class="flex flex-wrap justify-center gap-8 md:gap-16 border-t border-white/10 pt-16"
        >
          <div class="flex items-center gap-3 text-gray-400">
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
              class="text-[#22c55e]"
            >
              <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z" />
            </svg>
            <span class="font-medium">Enterprise Security</span>
          </div>
          <div class="flex items-center gap-3 text-gray-400">
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
              class="text-[#22c55e]"
            >
              <rect x="2" y="3" width="20" height="14" rx="2" ry="2" />
              <line x1="8" y1="21" x2="16" y2="21" />
              <line x1="12" y1="17" x2="12" y2="21" />
            </svg>
            <span class="font-medium">99.9% Uptime SLA</span>
          </div>
          <div class="flex items-center gap-3 text-gray-400">
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
              class="text-[#22c55e]"
            >
              <path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z" />
            </svg>
            <span class="font-medium">Real-time Sync</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-24 bg-[#0A0A0A] relative">
      <div class="w-full max-w-[1280px] mx-auto px-4">
        <div class="text-center mb-16 flex flex-col items-center">
          <span
            class="text-[#07B300] font-semibold tracking-wider text-sm uppercase mb-4"
          >
            Testimonials
          </span>
          <h2
            class="text-3xl md:text-6xl font-bold text-white mb-6 leading-tight"
          >
            Loved by Event <br class="hidden md:block" />
            <span class="text-[#07B300]">Organizers Worldwide</span>
          </h2>
          <p class="text-gray-400 text-xl max-w-2xl">
            Join thousands of organizers who trust EventNest to power their
            events.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
          <!-- Testimonial 1 -->
          <div
            class="p-8 rounded-2xl bg-black border border-white/10 hover:border-[#22c55e]/30 transition-all duration-300"
          >
            <div class="flex gap-1 mb-6 text-[#07B300]">
              <svg
                v-for="i in 5"
                :key="i"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="currentColor"
              >
                <path
                  d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
                />
              </svg>
            </div>
            <p class="text-gray-300 text-lg mb-8 leading-relaxed">
              "EventNest transformed how we manage our annual conference. The
              ticketing and check-in process is incredibly smooth."
            </p>
            <div class="flex items-center gap-4">
              <img
                src="https://randomuser.me/api/portraits/women/44.jpg"
                alt="Sarah Chen"
                class="w-12 h-12 rounded-full border-2 border-[#22c55e]/20"
              />
              <div>
                <div class="text-white font-bold text-lg">Sarah Chen</div>
                <div class="text-gray-500 text-base">
                  Event Director, TechConf Global
                </div>
              </div>
            </div>
          </div>

          <!-- Testimonial 2 -->
          <div
            class="p-8 rounded-2xl bg-black border border-white/10 hover:border-[#22c55e]/30 transition-all duration-300"
          >
            <div class="flex gap-1 mb-6 text-[#07B300]">
              <svg
                v-for="i in 5"
                :key="i"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="currentColor"
              >
                <path
                  d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
                />
              </svg>
            </div>
            <p class="text-gray-300 text-lg mb-8 leading-relaxed">
              "The analytics dashboard gives us insights we never had before.
              We've increased our ticket sales by 40% since switching."
            </p>
            <div class="flex items-center gap-4">
              <img
                src="https://randomuser.me/api/portraits/men/32.jpg"
                alt="Marcus Johnson"
                class="w-12 h-12 rounded-full border-2 border-[#22c55e]/20"
              />
              <div>
                <div class="text-white font-bold text-lg">Marcus Johnson</div>
                <div class="text-gray-500 text-base">
                  Founder, Music Festival Co
                </div>
              </div>
            </div>
          </div>

          <!-- Testimonial 3 -->
          <div
            class="p-8 rounded-2xl bg-black border border-white/10 hover:border-[#22c55e]/30 transition-all duration-300"
          >
            <div class="flex gap-1 mb-6 text-[#07B300]">
              <svg
                v-for="i in 5"
                :key="i"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="currentColor"
              >
                <path
                  d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
                />
              </svg>
            </div>
            <p class="text-gray-300 text-lg mb-8 leading-relaxed">
              "As a small event organizer, the free tier gives me everything I
              need. The platform is intuitive and powerful."
            </p>
            <div class="flex items-center gap-4">
              <img
                src="https://randomuser.me/api/portraits/women/65.jpg"
                alt="Emily Rodriguez"
                class="w-12 h-12 rounded-full border-2 border-[#22c55e]/20"
              />
              <div>
                <div class="text-white font-bold text-lg">Emily Rodriguez</div>
                <div class="text-gray-500 text-base">
                  Community Manager, Local Meetups
                </div>
              </div>
            </div>
          </div>

          <!-- Testimonial 4 -->
          <div
            class="p-8 rounded-2xl bg-black border border-white/10 hover:border-[#22c55e]/30 transition-all duration-300"
          >
            <div class="flex gap-1 mb-6 text-[#07B300]">
              <svg
                v-for="i in 5"
                :key="i"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="currentColor"
              >
                <path
                  d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
                />
              </svg>
            </div>
            <p class="text-gray-300 text-lg mb-8 leading-relaxed">
              "The customer support is exceptional. They helped us set up a
              complex multi-venue event in just days."
            </p>
            <div class="flex items-center gap-4">
              <img
                src="https://randomuser.me/api/portraits/men/86.jpg"
                alt="David Park"
                class="w-12 h-12 rounded-full border-2 border-[#22c55e]/20"
              />
              <div>
                <div class="text-white font-bold text-lg">David Park</div>
                <div class="text-gray-500 text-base">
                  Operations Lead, Convention Center
                </div>
              </div>
            </div>
          </div>

          <!-- Testimonial 5 -->
          <div
            class="p-8 rounded-2xl bg-black border border-white/10 hover:border-[#22c55e]/30 transition-all duration-300"
          >
            <div class="flex gap-1 mb-6 text-[#07B300]">
              <svg
                v-for="i in 5"
                :key="i"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="currentColor"
              >
                <path
                  d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
                />
              </svg>
            </div>
            <p class="text-gray-300 text-lg mb-8 leading-relaxed">
              "We moved from a legacy system and the migration was seamless.
              EventNest's modern approach is refreshing."
            </p>
            <div class="flex items-center gap-4">
              <img
                src="https://randomuser.me/api/portraits/women/24.jpg"
                alt="Lisa Thompson"
                class="w-12 h-12 rounded-full border-2 border-[#22c55e]/20"
              />
              <div>
                <div class="text-white font-bold text-lg">Lisa Thompson</div>
                <div class="text-gray-500 text-base">CTO, Events Inc</div>
              </div>
            </div>
          </div>

          <!-- Testimonial 6 -->
          <div
            class="p-8 rounded-2xl bg-black border border-white/10 hover:border-[#22c55e]/30 transition-all duration-300"
          >
            <div class="flex gap-1 mb-6 text-[#07B300]">
              <svg
                v-for="i in 5"
                :key="i"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="currentColor"
              >
                <path
                  d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
                />
              </svg>
            </div>
            <p class="text-gray-300 text-lg mb-8 leading-relaxed">
              "The mobile check-in app works flawlessly, even with thousands of
              attendees. A game-changer for our stadium events."
            </p>
            <div class="flex items-center gap-4">
              <img
                src="https://randomuser.me/api/portraits/men/46.jpg"
                alt="James Wilson"
                class="w-12 h-12 rounded-full border-2 border-[#22c55e]/20"
              />
              <div>
                <div class="text-white font-bold text-lg">James Wilson</div>
                <div class="text-gray-500 text-base">
                  Stadium Manager, Metro Arena
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing Section -->
    <section class="py-24 bg-black relative overflow-hidden" id="pricing">
      <div class="w-full max-w-[1280px] mx-auto px-4">
        <div class="text-center mb-16 flex flex-col items-center">
          <span
            class="text-[#07B300] font-semibold tracking-wider text-sm uppercase mb-4"
          >
            Pricing
          </span>
          <h2
            class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight"
          >
            Simple, Transparent <span class="text-[#07B300]">Pricing</span>
          </h2>
          <p class="text-gray-400 text-xl max-w-2xl">
            Choose the plan that fits your needs. No hidden fees, no surprises.
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
          <!-- Starter Plan -->
          <div
            class="p-8 rounded-3xl bg-[#0A0A0A] border border-white/5 flex flex-col items-center text-center group hover:border-white/10 transition-all duration-300"
          >
            <h3 class="text-2xl font-bold text-white mb-2">Starter</h3>
            <p class="text-gray-500 text-sm mb-8">
              Perfect for small events and getting started.
            </p>
            <div class="flex items-baseline gap-1 mb-10">
              <span class="text-4xl font-bold text-white">Free</span>
              <span class="text-gray-500">/forever</span>
            </div>
            <ul class="w-full space-y-4 mb-10 text-left">
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Up to 100 attendees per event
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Basic ticketing
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Email notifications
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Standard support
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Basic analytics
              </li>
            </ul>
            <NuxtLink
              to="/signup"
              class="w-full py-4 rounded-xl border border-white/10 text-white font-semibold hover:bg-white/5 transition-all mt-auto flex justify-center items-center"
            >
              Get Started
            </NuxtLink>
          </div>

          <!-- Professional Plan (Featured) -->
          <div
            class="p-8 rounded-3xl bg-[#0A0A0A] border-2 border-[#07B300] flex flex-col items-center text-center relative shadow-[0_0_40px_-15px_rgba(7,179,0,0.3)] group"
          >
            <div
              class="absolute -top-4 left-1/2 -translate-x-1/2 px-4 py-1.5 rounded-full bg-[#07B300] text-black text-sm font-bold flex items-center gap-1.5"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="14"
                height="14"
                viewBox="0 0 24 24"
                fill="currentColor"
              >
                <path
                  d="m12 15-3.03 2.02 1.09-3.39L7.24 11.5l3.47-.07L12 8l1.29 3.43 3.47.07-2.82 2.13 1.09 3.39z"
                />
              </svg>
              Most Popular
            </div>
            <h3 class="text-2xl font-bold text-white mb-2 mt-4">
              Professional
            </h3>
            <p class="text-gray-500 text-sm mb-8">
              For growing organizers with regular events.
            </p>
            <div class="flex items-baseline gap-1 mb-10">
              <span class="text-4xl font-bold text-white">$29</span>
              <span class="text-gray-500">/per event</span>
            </div>
            <ul class="w-full space-y-4 mb-10 text-left">
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Up to 1,000 attendees per event
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Advanced ticketing options
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Custom branding
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Priority support
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Advanced analytics
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Promo codes & discounts
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Waitlist management
              </li>
            </ul>
            <button
              class="w-full py-4 rounded-xl bg-[#07B300] text-black font-bold hover:bg-[#16a34a] transition-all mt-auto"
            >
              Start Free Trial
            </button>
          </div>

          <!-- Enterprise Plan -->
          <div
            class="p-8 rounded-3xl bg-[#0A0A0A] border border-white/5 flex flex-col items-center text-center group hover:border-white/10 transition-all duration-300"
          >
            <h3 class="text-2xl font-bold text-white mb-2">Enterprise</h3>
            <p class="text-gray-500 text-sm mb-8">
              For large-scale events and organizations.
            </p>
            <div class="flex items-baseline gap-1 mb-10">
              <span class="text-4xl font-bold text-white">Custom</span>
              <span class="text-gray-500">/contact us</span>
            </div>
            <ul class="w-full space-y-4 mb-10 text-left">
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Unlimited attendees
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                White-label solution
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Dedicated account manager
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                24/7 phone support
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Custom integrations
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                SLA guarantee
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                On-site support available
              </li>
              <li class="flex items-center gap-3 text-gray-400">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="#07B300"
                  stroke-width="3"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <polyline points="20 6 9 17 4 12" />
                </svg>
                Multi-event management
              </li>
            </ul>
            <button
              class="w-full py-4 rounded-xl border border-white/10 text-white font-semibold hover:bg-white/5 transition-all mt-auto"
            >
              Contact Sales
            </button>
          </div>
        </div>

        <div class="text-center">
          <p class="text-gray-500">
            Have questions?
            <a href="#faq" class="text-[#07B300] hover:underline font-medium"
              >Check our FAQ</a
            >
          </p>
        </div>
      </div>
    </section>

    <!-- FAQ Section -->
    <section class="py-24 bg-black relative" id="faq">
      <div class="w-full max-w-[1280px] mx-auto px-4">
        <div class="mb-16 text-left">
          <span
            class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-[#07B300]/10 border border-[#07B300]/20 text-[#07B300] text-sm font-medium mb-6"
          >
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
            >
              <circle cx="12" cy="12" r="10" />
              <path d="M9.09 9a3 3 0 0 1 5.83 1c0 2-3 3-3 3" />
              <path d="M12 17h.01" />
            </svg>
            FAQ
          </span>
          <h2 class="text-3xl md:text-6xl font-bold text-white mb-6">
            Frequently Asked <span class="text-[#07B300]">Questions</span>
          </h2>
          <p class="text-gray-400 text-lg md:text-xl max-w-3xl mb-4">
            Everything you need to know about EventNest. Can't find what you're
            looking for? Contact our support team.
          </p>
          <a
            href="#"
            class="inline-flex items-center gap-2 text-[#07B300] font-semibold hover:underline group"
          >
            Contact Support
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
              class="transition-transform group-hover:translate-x-1 group-hover:-translate-y-1"
            >
              <line x1="7" y1="17" x2="17" y2="7" />
              <polyline points="7 7 17 7 17 17" />
            </svg>
          </a>
        </div>

        <!-- FAQ Accordion -->
        <div
          class="w-full border border-white/5 rounded-2xl bg-[#050505]/50 backdrop-blur-sm overflow-hidden"
        >
          <div
            v-for="(item, index) in faqData"
            :key="index"
            class="border-b border-white/5 last:border-0"
          >
            <button
              @click="toggleFaq(index)"
              class="w-full flex items-center justify-between p-6 md:p-8 text-left hover:bg-white/[0.02] transition-all group"
            >
              <span
                class="text-lg md:text-xl font-medium transition-colors pr-8"
                :class="
                  activeIndex === index
                    ? 'text-[#07B300]'
                    : 'text-white group-hover:text-[#07B300]'
                "
              >
                {{ item.question }}
              </span>
              <div
                class="flex-shrink-0 w-10 h-10 rounded-full border border-white/10 flex items-center justify-center transition-all duration-300 bg-white/5"
                :class="{
                  'rotate-180 bg-white/10 border-white/20':
                    activeIndex === index,
                }"
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
                  :class="
                    activeIndex === index ? 'text-white' : 'text-[#07B300]'
                  "
                >
                  <path d="m6 9 6 6 6-6" />
                </svg>
              </div>
            </button>
            <div
              v-if="activeIndex === index"
              class="px-6 md:px-8 pb-8 animate-fade-in"
            >
              <p class="text-gray-400 text-lg leading-relaxed max-w-4xl">
                {{ item.answer }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Final CTA Section -->
    <section class="py-24 bg-black relative overflow-hidden">
      <div
        class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-[#07B300]/10 rounded-full blur-[120px] pointer-events-none"
      ></div>

      <div class="w-full max-w-[1280px] mx-auto px-4 relative z-10">
        <div class="flex flex-col items-center text-center">
          <!-- Badge -->
          <div
            class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-[#07B300]/10 border border-[#07B300]/20 text-[#07B300] text-sm font-medium mb-8"
          >
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
            >
              <path d="M6 2L3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4Z" />
              <path d="M3 6h18" />
              <path d="M16 10a4 4 0 0 1-8 0" />
            </svg>
            Start for Free
          </div>

          <!-- Headline -->
          <h2
            class="text-4xl md:text-7xl font-bold text-white mb-8 leading-[1.1]"
          >
            Ready to Create <br />
            Your <span class="text-[#07B300]">Next Event?</span>
          </h2>

          <!-- Description -->
          <p class="text-gray-400 text-lg md:text-xl max-w-2xl mb-12">
            Join thousands of organizers who use EventNest to create
            unforgettable experiences. Get started in minutes, no credit card
            required.
          </p>

          <!-- Action Buttons -->
          <div class="flex flex-col sm:flex-row gap-4 mb-16">
            <NuxtLink
              to="/signup"
              class="px-8 py-4 rounded-xl bg-[#07B300] hover:bg-[#16a34a] text-black font-bold flex items-center justify-center gap-2 transition-all shadow-[0_0_20px_-5px_rgba(7,179,0,0.4)]"
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
                <rect width="18" height="18" x="3" y="4" rx="2" ry="2" />
                <line x1="16" x2="16" y1="2" y2="6" />
                <line x1="8" x2="8" y1="2" y2="6" />
                <line x1="3" x2="21" y1="10" y2="10" />
              </svg>
              Create Your First Event
            </NuxtLink>
            <button
              class="px-8 py-4 rounded-xl border border-white/10 text-white font-semibold hover:bg-white/5 transition-all flex items-center justify-center gap-2"
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
                <line x1="5" y1="12" x2="19" y2="12" />
                <polyline points="12 5 19 12 12 19" />
              </svg>
            </button>
          </div>

          <!-- Trust Badges -->
          <div class="flex flex-wrap justify-center gap-8 md:gap-12">
            <div class="flex items-center gap-2 text-gray-500 text-sm">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                viewBox="0 0 24 24"
                fill="none"
                stroke="#07B300"
                stroke-width="2.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z" />
              </svg>
              SSL Secured
            </div>
            <div class="flex items-center gap-2 text-gray-500 text-sm">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                viewBox="0 0 24 24"
                fill="none"
                stroke="#07B300"
                stroke-width="2.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <polyline points="20 6 9 17 4 12" />
              </svg>
              GDPR Compliant
            </div>
            <div class="flex items-center gap-2 text-gray-500 text-sm">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                viewBox="0 0 24 24"
                fill="none"
                stroke="#07B300"
                stroke-width="2.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <path d="M3 3v18h18" />
                <path d="M18 17V9" />
                <path d="M13 17V5" />
                <path d="M8 17v-3" />
              </svg>
              99.9% Uptime
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style>
/* Custom animations if Tailwind config doesn't cover them */
body {
  font-family: "Inter", sans-serif;
}

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

.animate-fade-in {
  animation: fadeIn 0.3s ease-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>

<script>
import faqData from "../data/faq.json";
import integrationsData from "../data/integrations.json";
import CountUp from "../components/count-up.vue";

export default {
  components: {
    CountUp,
  },
  data() {
    return {
      activeIndex: null,
      selectedIntegrationIndex: 0,
      faqData,
      integrations: integrationsData,
      searchQuery: "",
      searchLocation: "",
    };
  },
  computed: {
    selectedIntegration() {
      return this.integrations[this.selectedIntegrationIndex];
    },
  },
  methods: {
    toggleFaq(index) {
      this.activeIndex = this.activeIndex === index ? null : index;
    },
    handleSearch() {
      // Build query parameters
      const params = new URLSearchParams();

      if (this.searchQuery.trim()) {
        params.append("q", this.searchQuery.trim());
      }

      if (this.searchLocation.trim()) {
        params.append("location", this.searchLocation.trim());
      }

      // Navigate to discover page with search parameters
      const queryString = params.toString();
      const url = queryString ? `/discover?${queryString}` : "/discover";

      this.$router.push(url);
    },
  },
};
</script>
