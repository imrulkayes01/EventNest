<template>
  <div
    class="min-h-screen bg-black text-white flex-col items-center justify-center pt-24 pb-20 overflow-hidden font-sans"
  >
    <!-- Content -->
    <section
      class="relative z-10 max-w-[1280px] mx-auto px-6 py-24 text-center"
    >
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

    <!-- Why Organizers Choose Us Section -->
    <section class="max-w-[1280px] mx-auto px-6 py-24 relative z-10">
      <div class="text-center mb-16 animate-slide-up">
        <h2
          class="text-[#07B300] text-xs font-bold tracking-[0.3em] uppercase mb-4"
        >
          Why Organizers Choose Us
        </h2>
        <h3 class="text-4xl md:text-[3.25rem] font-bold mb-6 leading-tight">
          More Than Just <span class="text-[#07B300]">Event Software</span>
        </h3>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
        <!-- Card 1: Low Fees -->
        <div
          class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#07B300]/20 transition-all duration-300 flex gap-6"
        >
          <div
            class="shrink-0 size-12 rounded-xl bg-[#07B300]/10 border border-[#07B300]/20 flex items-center justify-center text-[#07B300]"
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
              <line x1="12" y1="1" x2="12" y2="23" />
              <path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6" />
            </svg>
          </div>
          <div>
            <h4 class="text-xl font-bold mb-3 text-white">
              Low Fees, High Value
            </h4>
            <p class="text-gray-400 leading-relaxed">
              Our transparent pricing means more revenue stays in your pocket.
              No hidden fees, ever.
            </p>
          </div>
        </div>

        <!-- Card 2: Grow Your Audience -->
        <div
          class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#07B300]/20 transition-all duration-300 flex gap-6"
        >
          <div
            class="shrink-0 size-12 rounded-xl bg-[#07B300]/10 border border-[#07B300]/20 flex items-center justify-center text-[#07B300]"
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
              <polyline points="23 6 13.5 15.5 8.5 10.5 1 18" />
              <polyline points="17 6 23 6 23 12" />
            </svg>
          </div>
          <div>
            <h4 class="text-xl font-bold mb-3 text-white">
              Grow Your Audience
            </h4>
            <p class="text-gray-400 leading-relaxed">
              Reach new attendees through our event discovery platform and
              marketing tools.
            </p>
          </div>
        </div>

        <!-- Card 3: Save Time -->
        <div
          class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#07B300]/20 transition-all duration-300 flex gap-6"
        >
          <div
            class="shrink-0 size-12 rounded-xl bg-[#07B300]/10 border border-[#07B300]/20 flex items-center justify-center text-[#07B300]"
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
              <path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z" />
            </svg>
          </div>
          <div>
            <h4 class="text-xl font-bold mb-3 text-white">Save Time</h4>
            <p class="text-gray-400 leading-relaxed">
              Automate repetitive tasks and manage everything from one intuitive
              dashboard.
            </p>
          </div>
        </div>

        <!-- Card 4: Professional Branding -->
        <div
          class="group p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 hover:border-[#07B300]/20 transition-all duration-300 flex gap-6"
        >
          <div
            class="shrink-0 size-12 rounded-xl bg-[#07B300]/10 border border-[#07B300]/20 flex items-center justify-center text-[#07B300]"
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
              <path d="M6 9H4.5a2.5 2.5 0 0 1 0-5H6" />
              <path d="M18 9h1.5a2.5 2.5 0 0 0 0-5H18" />
              <path d="M4 22h16" />
              <path
                d="M10 14.66V17c0 .55-.47.98-.97 1.21C7.85 18.75 7 20.24 7 22"
              />
              <path
                d="M14 14.66V17c0 .55.47.98.97 1.21C16.15 18.75 17 20.24 17 22"
              />
              <path d="M18 2H6v7a6 6 0 0 0 12 0V2z" />
            </svg>
          </div>
          <div>
            <h4 class="text-xl font-bold mb-3 text-white">
              Professional Branding
            </h4>
            <p class="text-gray-400 leading-relaxed">
              Custom event pages and emails that match your brand identity
              perfectly.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section class="max-w-[1280px] mx-auto px-6 py-24 relative z-10">
      <div class="text-center mb-16 animate-slide-up">
        <h2
          class="text-[#07B300] text-xs font-bold tracking-[0.3em] uppercase mb-4"
        >
          Testimonials
        </h2>
        <h3 class="text-4xl md:text-[3.25rem] font-bold mb-6 leading-tight">
          Loved by <span class="text-[#07B300]">Event Organizers</span>
        </h3>
        <p class="text-gray-400 text-lg max-w-2xl mx-auto">
          Don't just take our word for it. Here's what organizers have to say
          about EventFlow.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Testimonial 1 -->
        <div
          class="p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 flex flex-col items-start text-left"
        >
          <div class="flex gap-1 mb-6 text-[#07B300]">
            <svg
              v-for="i in 5"
              :key="i"
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="18"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
              />
            </svg>
          </div>
          <p class="text-gray-300 text-lg leading-relaxed mb-8 italic">
            "EventFlow transformed how we manage our monthly meetups. The
            check-in process is so smooth, and the analytics help us understand
            our audience better."
          </p>
          <div>
            <h5 class="text-white font-bold text-lg">Sarah Chen</h5>
            <p class="text-gray-500 text-sm">
              Community Manager at Tech Meetup Network
            </p>
          </div>
        </div>

        <!-- Testimonial 2 -->
        <div
          class="p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 flex flex-col items-start text-left"
        >
          <div class="flex gap-1 mb-6 text-[#07B300]">
            <svg
              v-for="i in 5"
              :key="i"
              xmlns="http://www.w3.org/2000/svg"
              width="18"
              height="18"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
              />
            </svg>
          </div>
          <p class="text-gray-300 text-lg leading-relaxed mb-8 italic">
            "We've hosted over 50 events with EventFlow. The platform scales
            beautifully from intimate workshops to conferences with 1000+
            attendees."
          </p>
          <div>
            <h5 class="text-white font-bold text-lg">Marcus Rodriguez</h5>
            <p class="text-gray-500 text-sm">
              Event Director at Future Forward Conferences
            </p>
          </div>
        </div>

        <!-- Testimonial 3 -->
        <div
          class="p-8 rounded-2xl bg-[#0A0A0A] border border-white/5 flex flex-col items-start text-left"
        >
          <div class="flex gap-1 mb-6 text-[#07B300]">
            <svg
              v-for="i in 5"
              :key="i"
              xmlns="http://www.w3.org/2000/vue"
              width="18"
              height="18"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"
              />
            </svg>
          </div>
          <p class="text-gray-300 text-lg leading-relaxed mb-8 italic">
            "The customer support is phenomenal. Any question we have is
            answered within hours, and they actually listen to feature
            requests."
          </p>
          <div>
            <h5 class="text-white font-bold text-lg">Emily Watson</h5>
            <p class="text-gray-500 text-sm">
              Founder at Creative Workshops Co.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing Section -->
    <section class="max-w-[1280px] mx-auto px-6 py-24 relative z-10">
      <div class="text-center mb-16 animate-slide-up">
        <h2
          class="text-[#07B300] text-xs font-bold tracking-[0.3em] uppercase mb-4"
        >
          Simple Pricing
        </h2>
        <h3 class="text-4xl md:text-[3.25rem] font-bold mb-6 leading-tight">
          Transparent Pricing, <span class="text-[#07B300]">No Surprises</span>
        </h3>
        <p class="text-gray-400 text-lg max-w-2xl mx-auto">
          Start free and only pay when you sell tickets. No monthly fees, no
          contracts.
        </p>
      </div>

      <div
        class="max-w-4xl mx-auto p-12 rounded-[2.5rem] bg-[#0A0A0A] border border-[#07B300]/20 relative overflow-hidden group"
      >
        <div
          class="absolute inset-0 bg-gradient-to-br from-[#07B300]/5 to-transparent pointer-none"
        ></div>

        <div class="relative z-10 text-center flex flex-col items-center">
          <div class="flex items-baseline gap-2 mb-2">
            <span class="text-6xl md:text-8xl font-bold text-[#07B300]"
              >5%</span
            >
            <span class="text-2xl md:text-3xl font-bold text-white"
              >+ Transaction Fee</span
            >
            <span class="text-gray-500 text-sm">(2.9% + $0.30)</span>
          </div>
          <p class="text-gray-400 mb-12">per ticket sold</p>

          <div
            class="grid grid-cols-1 md:grid-cols-2 gap-x-16 gap-y-4 text-left mb-12 w-full max-w-2xl"
          >
            <div
              v-for="feature in pricingFeatures"
              :key="feature"
              class="flex items-center gap-3 text-gray-300"
            >
              <div
                class="size-5 rounded-full bg-[#07B300]/10 flex items-center justify-center text-[#07B300]"
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
              {{ feature }}
            </div>
          </div>

          <div class="flex flex-col sm:flex-row gap-4 w-full justify-center">
            <button
              class="bg-[#07B300] hover:bg-[#16a34a] text-black font-bold px-10 py-4 rounded-xl transition-all text-lg active:scale-95"
            >
              Get Started Free
            </button>
            <button
              class="bg-transparent border border-white/10 hover:bg-white/5 text-white font-bold px-10 py-4 rounded-xl transition-all text-lg active:scale-95"
            >
              View Full Pricing
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- Support Section -->
    <section
      class="max-w-[1280px] mx-auto px-6 py-24 relative z-10 text-center"
    >
      <div
        class="inline-flex size-16 rounded-2xl bg-[#07B300]/10 border border-[#07B300]/20 items-center justify-center text-[#07B300] mb-8"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <path d="M3 18v-6a9 9 0 0 1 18 0v6" />
          <path
            d="M21 19a2 2 0 0 1-2 2h-1a2 2 0 0 1-2-2v-3a2 2 0 0 1 2-2h3zM3 19a2 2 0 0 0 2 2h1a2 2 0 0 0 2-2v-3a2 2 0 0 0-2-2H3z"
          />
        </svg>
      </div>
      <h3 class="text-4xl md:text-5xl font-bold mb-6">
        <span class="text-[#07B300]">World-Class Support</span> <br />
        When You Need It
      </h3>
      <p class="text-gray-400 text-lg max-w-2xl mx-auto mb-10">
        Our dedicated support team is here to help you succeed. Whether you're
        hosting your first event or your hundredth, we've got your back.
      </p>

      <div class="flex flex-wrap justify-center gap-x-12 gap-y-4 mb-24">
        <div
          v-for="item in supportItems"
          :key="item"
          class="flex items-center gap-2 text-gray-300"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="18"
            height="18"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="3"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="text-[#07B300]"
          >
            <polyline points="20 6 9 17 4 12" />
          </svg>
          {{ item }}
        </div>
      </div>

      <!-- Final CTA -->
      <div
        class="relative py-20 px-6 rounded-[3rem] bg-gradient-to-b from-[#0A0A0A] to-transparent border-t border-white/5"
      >
        <div
          class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full border border-green-500/20 bg-green-500/10 text-green-400 text-xs font-bold mb-8"
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
            <path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2" />
            <circle cx="9" cy="7" r="4" />
            <path d="M22 21v-2a4 4 0 0 0-3-3.87" />
            <path d="M16 3.13a4 4 0 0 1 0 7.75" />
          </svg>
          Join 50,000+ Organizers
        </div>
        <h3 class="text-4xl md:text-6xl font-bold mb-6">
          Ready to Create Your <span class="text-[#07B300]">First Event?</span>
        </h3>
        <p class="text-gray-400 text-xl max-w-2xl mx-auto mb-12">
          Start free today and see why thousands of organizers trust EventFlow
          for their events.
        </p>

        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <button
            class="bg-[#07B300] hover:bg-[#16a34a] text-black font-bold px-10 py-4 rounded-xl transition-all text-lg active:scale-95 flex items-center justify-center gap-2"
          >
            Get Started Free
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
          <button
            class="bg-transparent border border-white/10 hover:bg-white/5 text-white font-bold px-10 py-4 rounded-xl transition-all text-lg active:scale-95"
          >
            Browse Events
          </button>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const pricingFeatures = [
  "Unlimited events",
  "Real-time analytics",
  "Email support",
  "Promo codes & discounts",
  "Mobile app access",
  "Custom branding",
  "QR code check-in",
  "Multiple ticket types",
  "Attendee management",
  "Secure payments",
];

const supportItems = [
  "24/7 email support",
  "Live chat available",
  "Comprehensive help center",
  "Video tutorials",
];
</script>

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
