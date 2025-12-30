<template>
  <div
    class="min-h-screen bg-black text-white font-sans flex flex-col md:flex-row"
  >
    <!-- Left Side: Branding & Testimonial -->
    <div
      class="hidden md:flex md:w-1/2 lg:w-2/5 p-12 flex-col justify-between relative overflow-hidden bg-[#050505]"
    >
      <!-- Background Gradient Effect -->
      <div
        class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[500px] h-[500px] bg-green-500/10 blur-[120px] rounded-full"
      ></div>

      <div class="relative z-10">
        <NuxtLink to="/" class="flex items-center gap-2 group">
          <div
            class="w-10 h-10 bg-[#22c55e] rounded-lg flex items-center justify-center group-hover:scale-110 transition-transform"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              stroke="black"
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
          <span class="text-2xl font-bold tracking-tight">EventFlow</span>
        </NuxtLink>
      </div>

      <div class="relative z-10 max-w-md">
        <blockquote
          class="text-2xl lg:text-3xl font-medium leading-relaxed mb-8"
        >
          "EventFlow made managing our annual tech conference effortless. The
          platform is intuitive and the support team is incredible."
        </blockquote>
        <div class="flex items-center gap-4">
          <img
            src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&q=80&w=150&h=150"
            alt="Alex Chen"
            class="w-12 h-12 rounded-full object-cover border-2 border-green-500/20"
          />
          <div>
            <div class="font-bold">Alex Chen</div>
            <div class="text-white/60 text-sm">Head of Events, TechCorp</div>
          </div>
        </div>
      </div>

      <div class="relative z-10 grid grid-cols-3 gap-8">
        <div>
          <div class="text-2xl lg:text-3xl font-bold text-[#22c55e]">50K+</div>
          <div class="text-xs uppercase tracking-wider text-white/40 mt-1">
            Events Created
          </div>
        </div>
        <div>
          <div class="text-2xl lg:text-3xl font-bold text-[#22c55e]">2M+</div>
          <div class="text-xs uppercase tracking-wider text-white/40 mt-1">
            Tickets Sold
          </div>
        </div>
        <div>
          <div class="text-2xl lg:text-3xl font-bold text-[#22c55e]">99.9%</div>
          <div class="text-xs uppercase tracking-wider text-white/40 mt-1">
            Uptime
          </div>
        </div>
      </div>
    </div>

    <!-- Right Side: Signup Form -->
    <div
      class="flex-1 p-6 md:p-12 lg:p-20 flex flex-col justify-center items-center bg-black overflow-y-auto"
    >
      <div class="w-full max-w-md">
        <NuxtLink
          to="/"
          class="inline-flex items-center gap-2 text-sm text-white/60 hover:text-white mb-8 transition-colors group"
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
            class="group-hover:-translate-x-1 transition-transform"
          >
            <line x1="19" x2="5" y1="12" y2="12" />
            <polyline points="12 19 5 12 12 5" />
          </svg>
          Back to home
        </NuxtLink>

        <h1 class="text-3xl font-bold mb-2">Create your account</h1>
        <p class="text-white/60 mb-8">Start creating unforgettable events</p>

        <form @submit.prevent="handleSignup" class="space-y-6">
          <!-- Role Selection -->
          <div class="space-y-3">
            <label class="text-sm font-medium text-white/80">I want to</label>
            <div class="grid grid-cols-2 gap-4">
              <button
                type="button"
                @click="role = 'attendee'"
                :class="[
                  'p-4 rounded-xl border-2 text-left transition-all group',
                  role === 'attendee'
                    ? 'border-[#22c55e] bg-green-500/5'
                    : 'border-white/10 hover:border-white/20 bg-white/5',
                ]"
              >
                <div
                  :class="[
                    'w-10 h-10 rounded-lg flex items-center justify-center mb-3 transition-colors',
                    role === 'attendee'
                      ? 'text-[#22c55e]'
                      : 'text-white/40 group-hover:text-white/60',
                  ]"
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
                    <path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2" />
                    <circle cx="12" cy="7" r="4" />
                  </svg>
                </div>
                <div class="font-bold">Attend Events</div>
                <div class="text-xs text-white/40">
                  Discover and buy tickets
                </div>
              </button>
              <button
                type="button"
                @click="role = 'host'"
                :class="[
                  'p-4 rounded-xl border-2 text-left transition-all group',
                  role === 'host'
                    ? 'border-[#22c55e] bg-green-500/5'
                    : 'border-white/10 hover:border-white/20 bg-white/5',
                ]"
              >
                <div
                  :class="[
                    'w-10 h-10 rounded-lg flex items-center justify-center mb-3 transition-colors',
                    role === 'host'
                      ? 'text-[#22c55e]'
                      : 'text-white/40 group-hover:text-white/60',
                  ]"
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
                    <rect width="16" height="16" x="4" y="4" rx="2" />
                    <line x1="9" x2="9" y1="9" y2="15" />
                    <line x1="12" x2="12" y1="9" y2="15" />
                    <line x1="15" x2="15" y1="9" y2="15" />
                  </svg>
                </div>
                <div class="font-bold">Host Events</div>
                <div class="text-xs text-white/40">
                  Create and manage events
                </div>
              </button>
            </div>
          </div>

          <!-- Name Inputs -->
          <div class="grid grid-cols-2 gap-4">
            <div class="space-y-2">
              <label class="text-sm font-medium text-white/80"
                >First name <span class="text-red-500">*</span></label
              >
              <input
                v-model="form.firstName"
                type="text"
                placeholder="John"
                required
                class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 focus:outline-none focus:border-[#22c55e] transition-colors"
              />
            </div>
            <div class="space-y-2">
              <label class="text-sm font-medium text-white/80"
                >Last name <span class="text-red-500">*</span></label
              >
              <input
                v-model="form.lastName"
                type="text"
                placeholder="Doe"
                required
                class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 focus:outline-none focus:border-[#22c55e] transition-colors"
              />
            </div>
          </div>

          <!-- Email -->
          <div class="space-y-2">
            <label class="text-sm font-medium text-white/80"
              >Email <span class="text-red-500">*</span></label
            >
            <div class="relative">
              <span
                class="absolute left-4 top-1/2 -translate-y-1/2 text-white/40"
              >
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
                >
                  <rect width="20" height="16" x="2" y="4" rx="2" />
                  <path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7" />
                </svg>
              </span>
              <input
                v-model="form.email"
                type="email"
                placeholder="you@example.com"
                required
                class="w-full bg-white/5 border border-white/10 rounded-lg pl-11 pr-4 py-3 focus:outline-none focus:border-[#22c55e] transition-colors"
              />
            </div>
          </div>

          <!-- Password -->
          <div class="space-y-2">
            <label class="text-sm font-medium text-white/80"
              >Password <span class="text-red-500">*</span></label
            >
            <div class="relative">
              <span
                class="absolute left-4 top-1/2 -translate-y-1/2 text-white/40"
              >
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
                >
                  <rect width="18" height="11" x="3" y="11" rx="2" ry="2" />
                  <path d="M7 11V7a5 5 0 0 1 10 0v4" />
                </svg>
              </span>
              <input
                v-model="form.password"
                :type="showPassword ? 'text' : 'password'"
                placeholder="Min. 8 characters"
                required
                class="w-full bg-white/5 border border-white/10 rounded-lg pl-11 pr-12 py-3 focus:outline-none focus:border-[#22c55e] transition-colors"
              />
              <button
                type="button"
                @click="showPassword = !showPassword"
                class="absolute right-4 top-1/2 -translate-y-1/2 text-white/40 hover:text-white transition-colors"
              >
                <svg
                  v-if="showPassword"
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path d="M9.88 9.88L4.62 4.62" />
                  <path d="M1 1l22 22" />
                  <path
                    d="M9.06 13.94c-1.63-1.63-1.63-4.28 0-5.91a4.11 4.11 0 0 1 1.62-1.03"
                  />
                  <path
                    d="M11.77 11.77C10.5 10.5 10.5 8.5 11.77 7.23a3.17 3.17 0 0 1 2.54-.92"
                  />
                  <path d="M14.78 14.78c1.63 1.63 4.28 1.63 5.91 0" />
                  <path d="M21.21 21.21l-3.21-3.21" />
                  <path d="M15.46 9.46c.75.75 1.15 1.75 1.15 2.54" />
                  <path d="M19 12a1 1 0 0 1-1 1" />
                  <path
                    d="M5.31 5.31c-.13.12-.26.25-.38.38A12 12 0 0 0 1.25 12c.5 1 1.5 3 4.5 5 3 2 6 2 9 0 .88-.59 1.66-1.28 2.34-2.06"
                  />
                  <path d="M22.75 12c-.5-1-1.5-3-4.5-5a12 12 0 0 0-4.06-1.89" />
                </svg>
                <svg
                  v-else
                  xmlns="http://www.w3.org/2000/svg"
                  width="18"
                  height="18"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path d="M2 12s3-7 10-7 10 7 10 7-3 7-10 7-10-7-10-7Z" />
                  <circle cx="12" cy="12" r="3" />
                </svg>
              </button>
            </div>
            <!-- Password Validation -->
            <ul class="mt-3 space-y-1.5">
              <li
                class="flex items-center gap-2 text-xs"
                :class="
                  passwordCriteria.length ? 'text-[#22c55e]' : 'text-white/40'
                "
              >
                <div
                  class="w-1.5 h-1.5 rounded-full border border-current"
                ></div>
                At least 8 characters
              </li>
              <li
                class="flex items-center gap-2 text-xs"
                :class="
                  passwordCriteria.uppercase
                    ? 'text-[#22c55e]'
                    : 'text-white/40'
                "
              >
                <div
                  class="w-1.5 h-1.5 rounded-full border border-current"
                ></div>
                At least one uppercase letter
              </li>
              <li
                class="flex items-center gap-2 text-xs"
                :class="
                  passwordCriteria.number ? 'text-[#22c55e]' : 'text-white/40'
                "
              >
                <div
                  class="w-1.5 h-1.5 rounded-full border border-current"
                ></div>
                At least one number
              </li>
            </ul>
          </div>

          <!-- Confirm Password -->
          <div class="space-y-2">
            <label class="text-sm font-medium text-white/80"
              >Confirm Password <span class="text-red-500">*</span></label
            >
            <div class="relative">
              <span
                class="absolute left-4 top-1/2 -translate-y-1/2 text-white/40"
              >
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
                >
                  <rect width="18" height="11" x="3" y="11" rx="2" ry="2" />
                  <path d="M7 11V7a5 5 0 0 1 10 0v4" />
                </svg>
              </span>
              <input
                v-model="form.confirmPassword"
                type="password"
                placeholder="Re-enter your password"
                required
                class="w-full bg-white/5 border border-white/10 rounded-lg pl-11 pr-4 py-3 focus:outline-none focus:border-[#22c55e] transition-colors"
              />
            </div>
          </div>

          <!-- TOS -->
          <label class="flex items-center gap-3 cursor-pointer group">
            <div class="relative flex items-center">
              <input
                type="checkbox"
                v-model="form.agree"
                required
                class="peer sr-only"
              />
              <div
                class="w-5 h-5 border-2 border-white/10 rounded peer-checked:bg-[#22c55e] peer-checked:border-[#22c55e] transition-all"
              ></div>
              <svg
                class="absolute w-3 h-3 text-black opacity-0 peer-checked:opacity-100 left-1 transition-opacity pointer-events-none"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="4"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <polyline points="20 6 9 17 4 12" />
              </svg>
            </div>
            <span class="text-xs text-white/60">
              I agree to the
              <a href="#" class="text-[#22c55e] hover:underline"
                >Terms of Service</a
              >
              and
              <a href="#" class="text-[#22c55e] hover:underline"
                >Privacy Policy</a
              >
            </span>
          </label>

          <!-- Submit Button -->
          <button
            type="submit"
            class="w-full bg-[#22c55e] hover:bg-[#16a34a] text-black font-bold py-4 rounded-xl transition-all hover:scale-[1.02] active:scale-[0.98]"
          >
            Create Account
          </button>

          <!-- Login Link -->
          <p class="text-center text-sm text-white/60">
            Already have an account?
            <NuxtLink
              to="/login"
              class="text-[#22c55e] hover:underline font-medium"
              >Sign in</NuxtLink
            >
          </p>
        </form>
      </div>
    </div>

    <!-- Floating Bubble (matching image) -->
    <div
      class="fixed bottom-6 right-6 w-14 h-14 bg-[#22c55e] rounded-full flex items-center justify-center shadow-lg shadow-green-500/20 cursor-pointer hover:scale-110 transition-transform"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        stroke="black"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <path d="m3 21 1.9-5.7a8.5 8.5 0 1 1 3.8 3.8z" />
      </svg>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: false,
});

const role = ref("attendee");
const showPassword = ref(false);

const form = reactive({
  firstName: "",
  lastName: "",
  email: "",
  password: "",
  confirmPassword: "",
  agree: false,
});

const passwordCriteria = computed(() => ({
  length: form.password.length >= 8,
  uppercase: /[A-Z]/.test(form.password),
  number: /[0-9]/.test(form.password),
}));

const handleSignup = () => {
  console.log("Form submitted:", form);
  // Implement signup logic
};
</script>

<style scoped>
/* Optional: Custom animations or tweaks */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

form {
  animation: fadeIn 0.5s ease-out;
}
</style>
