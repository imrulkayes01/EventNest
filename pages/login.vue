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
          "Logging into EventFlow feels like coming home. Everything I need to
          manage my events is right at my fingertips."
        </blockquote>
        <div class="flex items-center gap-4">
          <img
            src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&q=80&w=150&h=150"
            alt="Michael Rodriguez"
            class="w-12 h-12 rounded-full object-cover border-2 border-green-500/20"
          />
          <div>
            <div class="font-bold">Michael Rodriguez</div>
            <div class="text-white/60 text-sm">Event Director, MusicFest</div>
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

    <!-- Right Side: Login Form -->
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

        <h1 class="text-3xl font-bold mb-2">Welcome back</h1>
        <p class="text-white/60 mb-8">Sign in to continue to EventFlow</p>

        <form @submit.prevent="handleLogin" class="space-y-6">
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
            <div class="flex items-center justify-between">
              <label class="text-sm font-medium text-white/80"
                >Password <span class="text-red-500">*</span></label
              >
              <NuxtLink
                to="/forgot-password"
                class="text-xs text-[#22c55e] hover:underline"
              >
                Forgot password?
              </NuxtLink>
            </div>
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
                placeholder="Enter your password"
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
          </div>

          <!-- Remember Me -->
          <label class="flex items-center gap-3 cursor-pointer group">
            <div class="relative flex items-center">
              <input
                type="checkbox"
                v-model="form.rememberMe"
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
            <span class="text-sm text-white/60"> Remember me </span>
          </label>

          <!-- Submit Button -->
          <button
            type="submit"
            class="w-full bg-[#22c55e] hover:bg-[#16a34a] text-black font-bold py-4 rounded-xl transition-all hover:scale-[1.02] active:scale-[0.98]"
          >
            Sign In
          </button>

          <!-- Divider -->
          <div class="relative">
            <div class="absolute inset-0 flex items-center">
              <div class="w-full border-t border-white/10"></div>
            </div>
            <div class="relative flex justify-center text-xs uppercase">
              <span class="bg-black px-2 text-white/40">Or continue with</span>
            </div>
          </div>

          <!-- Social Login -->
          <div class="grid grid-cols-2 gap-4">
            <button
              type="button"
              @click="handleSocialLogin('google')"
              class="flex items-center justify-center gap-2 bg-white/5 hover:bg-white/10 border border-white/10 rounded-lg px-4 py-3 transition-all group"
            >
              <svg
                class="w-5 h-5"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"
                  fill="#4285F4"
                />
                <path
                  d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"
                  fill="#34A853"
                />
                <path
                  d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z"
                  fill="#FBBC05"
                />
                <path
                  d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z"
                  fill="#EA4335"
                />
              </svg>
              <span class="text-sm font-medium">Google</span>
            </button>
            <button
              type="button"
              @click="handleSocialLogin('github')"
              class="flex items-center justify-center gap-2 bg-white/5 hover:bg-white/10 border border-white/10 rounded-lg px-4 py-3 transition-all group"
            >
              <svg
                class="w-5 h-5"
                viewBox="0 0 24 24"
                fill="currentColor"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M12 2C6.477 2 2 6.477 2 12c0 4.42 2.865 8.17 6.839 9.49.5.092.682-.217.682-.482 0-.237-.008-.866-.013-1.7-2.782.603-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.463-1.11-1.463-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.831.092-.646.35-1.086.636-1.336-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0112 6.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.578.688.48C19.138 20.167 22 16.418 22 12c0-5.523-4.477-10-10-10z"
                />
              </svg>
              <span class="text-sm font-medium">GitHub</span>
            </button>
          </div>

          <!-- Signup Link -->
          <p class="text-center text-sm text-white/60">
            Don't have an account?
            <NuxtLink
              to="/signup"
              class="text-[#22c55e] hover:underline font-medium"
              >Sign up</NuxtLink
            >
          </p>
        </form>
      </div>
    </div>

    <!-- Floating Bubble (matching signup) -->
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

const showPassword = ref(false);

const form = reactive({
  email: "",
  password: "",
  rememberMe: false,
});

const handleLogin = () => {
  console.log("Login form submitted:", form);
  // Implement login logic here
  // For now, we'll just log the form data
  // You can add authentication logic, API calls, etc.
};

const handleSocialLogin = (provider) => {
  console.log(`Social login with ${provider}`);
  // Implement social login logic here
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
