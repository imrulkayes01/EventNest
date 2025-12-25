<template>
  <span>{{ displayValue }}{{ suffix }}</span>
</template>

<script>
export default {
  name: "CountUp",
  props: {
    end: {
      type: [Number, String],
      required: true,
    },
    duration: {
      type: Number,
      default: 2000,
    },
    suffix: {
      type: String,
      default: "",
    },
    decimals: {
      type: Number,
      default: 0,
    },
  },
  data() {
    return {
      currentValue: 0,
      startTime: null,
      displayValue: "0",
      observer: null,
    };
  },
  mounted() {
    this.observer = new IntersectionObserver(
      (entries) => {
        if (entries[0].isIntersecting) {
          this.startAnimation();
          this.observer.disconnect();
        }
      },
      { threshold: 0.1 }
    );

    this.observer.observe(this.$el);
  },
  methods: {
    startAnimation() {
      const endValue = parseFloat(this.end.toString().replace(/,/g, ""));
      const step = (timestamp) => {
        if (!this.startTime) this.startTime = timestamp;
        const progress = Math.min(
          (timestamp - this.startTime) / this.duration,
          1
        );

        this.currentValue = progress * endValue;

        // Format with thousands separator and decimals
        this.displayValue = this.currentValue.toLocaleString(undefined, {
          minimumFractionDigits: this.decimals,
          maximumFractionDigits: this.decimals,
        });

        if (progress < 1) {
          window.requestAnimationFrame(step);
        } else {
          // Final accurate value
          this.displayValue = endValue.toLocaleString(undefined, {
            minimumFractionDigits: this.decimals,
            maximumFractionDigits: this.decimals,
          });
        }
      };
      window.requestAnimationFrame(step);
    },
  },
  beforeUnmount() {
    if (this.observer) this.observer.disconnect();
  },
};
</script>
