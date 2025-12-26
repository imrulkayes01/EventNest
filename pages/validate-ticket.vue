<template>
  <div
    class="min-h-screen bg-black text-white selection:bg-[#07B300] selection:text-black font-sans relative overflow-hidden flex flex-col items-center justify-center px-4 py-24"
  >
    <!-- Content Wrapper -->
    <div
      class="relative z-10 w-full max-w-2xl flex flex-col items-center animate-fade-in shadow-2xl"
    >
      <!-- Logo Container -->
      <div class="mb-6 relative">
        <div
          class="absolute inset-0 bg-[#07B300]/20 blur-2xl rounded-full"
        ></div>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="54"
          height="54"
          viewBox="0 0 24 24"
          fill="none"
          class="relative z-10 drop-shadow-[0_0_15px_rgba(7,179,0,0.6)]"
        >
          <path
            d="M7 6H5C3.89543 6 3 6.89543 3 8V16C3 17.1046 3.89543 18 5 18H7"
            stroke="#07B300"
            stroke-width="2.5"
            stroke-linecap="round"
          />
          <path
            d="M17 6H19C20.1046 6 21 6.89543 21 8V16C21 17.1046 20.1046 18 19 18H17"
            stroke="#07B300"
            stroke-width="2.5"
            stroke-linecap="round"
          />
          <path
            d="M10 6V8M10 11V13M10 16V18"
            stroke="#07B300"
            stroke-width="2.5"
            stroke-linecap="round"
          />
          <path
            d="M14 6V8M14 11V13M14 16V18"
            stroke="#07B300"
            stroke-width="2.5"
            stroke-linecap="round"
          />
        </svg>
      </div>

      <!-- Heading Section -->
      <div class="text-center pb-6">
        <h1 class="text-4xl md:text-6xl font-bold mb-6">
          Validate <span class="text-[#07B300]">Ticket</span>
        </h1>
        <p
          class="text-gray-400 text-lg md:text-xl font-medium leading-relaxed opacity-80"
        >
          Enter a ticket number or QR code to verify its authenticity
        </p>
      </div>

      <!-- Main Interaction Card -->
      <div
        class="w-full bg-[#0A0A0A] border border-white/10 rounded-[32px] p-8 md:p-12 mb-8 relative overflow-hidden group shadow-2xl"
      >
        <!-- Subtle gradient overlay -->
        <div
          class="absolute inset-0 bg-gradient-to-br from-white/[0.03] to-transparent pointer-events-none"
        ></div>

        <div class="relative z-10">
          <div class="mb-10">
            <h2 class="text-2xl font-bold text-white mb-3">
              Check Ticket Status
            </h2>
            <p class="text-gray-500 text-sm leading-relaxed">
              This is a public tool. Anyone can verify if a ticket is valid
              without needing to log in.
            </p>
          </div>

          <div class="space-y-8">
            <div class="relative">
              <label
                class="block text-sm font-bold text-gray-400 mb-3 tracking-widest uppercase"
              >
                Ticket Number or QR Code
              </label>
              <div class="relative">
                <input
                  type="text"
                  placeholder="e.g., TKT-1-A3F9K2M7 or QR Code"
                  class="w-full bg-black border border-white/10 rounded-2xl px-6 py-5 placeholder-white/10 focus:outline-none text-lg"
                />
              </div>
              <div class="mt-4 flex items-start gap-3 px-1">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  class="text-[#07B300]/50 mt-0.5"
                >
                  <circle cx="12" cy="12" r="10" />
                  <path d="M12 16v-4" />
                  <path d="M12 8h.01" />
                </svg>
                <p class="text-gray-600 text-sm leading-snug">
                  Enter the ticket number (e.g., TKT-1-ABC12345) or paste the QR
                  code value
                </p>
              </div>
            </div>

            <button
              class="w-full bg-[#07B300] hover:bg-[#07B300]/90 text-black font-bold py-5 rounded-2xl transition-all duration-300 active:scale-[0.97] text-xl tracking-tight"
            >
              Validate Ticket
            </button>
          </div>
        </div>
      </div>

      <!-- Information Card -->
      <div
        class="w-full bg-white/[0.02] border border-white/5 rounded-[24px] p-8 md:p-10 backdrop-blur-md transition-colors hover:bg-white/[0.04]"
      >
        <h3
          class="text-gray-300 font-bold text-lg mb-4 flex items-center gap-2"
        >
          Note:
        </h3>
        <p
          class="text-gray-500 text-base md:text-lg leading-relaxed font-medium"
        >
          This tool only validates the ticket's authenticity. For check-in at
          the event, please present your ticket to the event organizer or
          security staff.
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.animate-fade-in {
  animation: fadeIn 1s cubic-bezier(0.19, 1, 0.22, 1) forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(40px) scale(0.98);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

/* Base styles to ensure consistency */
:deep(input)::placeholder {
  font-weight: 400;
}
</style>
