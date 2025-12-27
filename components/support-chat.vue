<template>
  <div class="fixed bottom-6 right-6 z-[100]">
    <!-- Chat Window -->
    <div
      v-if="isOpen"
      class="mb-4 w-[380px] h-[500px] bg-[#0A0A0A] border border-white/10 rounded-2xl shadow-2xl flex flex-col overflow-hidden animate-fade-in"
    >
      <!-- Header -->
      <div
        class="p-4 bg-white/5 border-b border-white/10 flex items-center justify-between"
      >
        <div class="flex items-center gap-3">
          <div class="relative">
            <div
              class="w-10 h-10 rounded-full bg-[#07B300] flex items-center justify-center text-black"
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
                <path
                  d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"
                />
              </svg>
            </div>
            <div
              class="absolute -bottom-0.5 -right-0.5 w-3 h-3 bg-[#07B300] border-2 border-[#0A0A0A] rounded-full"
            ></div>
          </div>
          <div>
            <h3 class="font-bold text-white text-sm">Support</h3>
            <p class="text-xs text-gray-500">Connecting...</p>
          </div>
        </div>
        <div class="flex items-center gap-2">
          <button
            @click="isOpen = false"
            class="p-1.5 hover:bg-white/5 rounded-lg text-gray-400 transition-colors"
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
              <path d="M8 3v3a2 2 0 0 1-2 2H3" />
              <path d="M21 8h-3a2 2 0 0 1-2-2V3" />
              <path d="M3 16h3a2 2 0 0 1 2 2v3" />
              <path d="M16 21v-3a2 2 0 0 1 2-2h3" />
            </svg>
          </button>
          <button
            @click="isOpen = false"
            class="p-1.5 hover:bg-white/5 rounded-lg text-gray-400 transition-colors"
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
              <path d="M18 6 6 18" />
              <path d="m6 6 12 12" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Messages Area -->
      <div
        class="flex-1 overflow-y-auto p-4 space-y-4 custom-scrollbar"
        ref="messageContainer"
      >
        <div
          v-for="(msg, index) in messages"
          :key="index"
          :class="[
            'flex flex-col',
            msg.type === 'user' ? 'items-end' : 'items-start',
          ]"
        >
          <div
            :class="[
              'max-w-[85%] p-3 rounded-2xl text-sm leading-relaxed mb-1',
              msg.type === 'user'
                ? 'bg-[#07B300] text-black rounded-tr-none font-medium'
                : 'bg-white/5 text-gray-200 border border-white/10 rounded-tl-none',
            ]"
          >
            {{ msg.text }}
          </div>
          <span class="text-[10px] text-gray-600 px-1">{{ msg.time }}</span>
        </div>
        <div v-if="isTyping" class="flex flex-col items-start">
          <div
            class="bg-white/5 text-gray-400 p-3 rounded-2xl rounded-tl-none border border-white/10"
          >
            <div class="flex gap-1">
              <span
                class="w-1.5 h-1.5 bg-gray-600 rounded-full animate-bounce"
              ></span>
              <span
                class="w-1.5 h-1.5 bg-gray-600 rounded-full animate-bounce delay-150"
              ></span>
              <span
                class="w-1.5 h-1.5 bg-gray-600 rounded-full animate-bounce delay-300"
              ></span>
            </div>
          </div>
        </div>
      </div>

      <!-- Input Area -->
      <div class="p-4 bg-white/5 border-t border-white/10">
        <form @submit.prevent="sendMessage" class="flex items-center gap-2">
          <input
            v-model="userInput"
            type="text"
            placeholder="Type a message..."
            class="flex-1 bg-black/50 border border-white/10 rounded-xl px-4 py-2.5 text-sm text-white placeholder-gray-600 focus:outline-none focus:border-[#07B300]/50 transition-colors"
          />
          <button
            type="submit"
            :disabled="!userInput.trim()"
            class="w-10 h-10 rounded-xl bg-[#07B300] hover:bg-[#16a34a] disabled:opacity-50 disabled:hover:bg-[#07B300] text-black flex items-center justify-center transition-all"
          >
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
            >
              <path d="m22 2-7 20-4-9-9-4Z" />
              <path d="M22 2 11 13" />
            </svg>
          </button>
        </form>
      </div>
    </div>

    <!-- Toggle Button -->
    <button
      @click="toggleChat"
      class="w-14 h-14 bg-[#07B300] hover:bg-[#16a34a] rounded-full shadow-lg shadow-[#22c55e]/30 flex items-center justify-center text-black transition-all hover:scale-110 active:scale-95"
    >
      <svg
        v-if="!isOpen"
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
      <svg
        v-else
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
        <path d="M18 6 6 18" />
        <path d="m6 6 12 12" />
      </svg>
    </button>
  </div>
</template>

<script>
export default {
  name: "SupportChat",
  data() {
    return {
      isOpen: false,
      userInput: "",
      isTyping: false,
      messages: [
        {
          type: "bot",
          text: "Hello! How can we help you today?",
          time: new Date().toLocaleTimeString([], {
            hour: "2-digit",
            minute: "2-digit",
          }),
        },
      ],
    };
  },
  methods: {
    toggleChat() {
      this.isOpen = !this.isOpen;
    },
    sendMessage() {
      if (!this.userInput.trim()) return;

      const userMsg = {
        type: "user",
        text: this.userInput,
        time: new Date().toLocaleTimeString([], {
          hour: "2-digit",
          minute: "2-digit",
        }),
      };
      this.messages.push(userMsg);
      const prevInput = this.userInput;
      this.userInput = "";

      this.scrollToBottom();

      // Bot Response Logic
      this.isTyping = true;

      setTimeout(() => {
        this.isTyping = false;
        const botMsg = {
          type: "bot",
          text: "Thanks for your message! A support agent will respond shortly. In the meantime, you can check our FAQ section for quick answers.",
          time: new Date().toLocaleTimeString([], {
            hour: "2-digit",
            minute: "2-digit",
          }),
        };
        this.messages.push(botMsg);
        this.scrollToBottom();
      }, 1500);
    },
    scrollToBottom() {
      this.$nextTick(() => {
        const container = this.$refs.messageContainer;
        if (container) {
          container.scrollTop = container.scrollHeight;
        }
      });
    },
  },
};
</script>

<style scoped>
.custom-scrollbar::-webkit-scrollbar {
  width: 4px;
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

.animate-fade-in {
  animation: fadeIn 0.3s ease-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px) scale(0.95);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

.delay-150 {
  animation-delay: 150ms;
}
.delay-300 {
  animation-delay: 300ms;
}
</style>
