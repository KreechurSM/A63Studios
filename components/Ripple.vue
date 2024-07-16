<template>
  <div
    class="inset-0 flex items-center justify-center bg-white/5 mask-image-linear-gradient-to-bottom from-white to-transparent"
    style="position: absolute; top: 50vh;">
    <div v-for="i in numCircles" :key="i" class="animate-ripple rounded-full bg-foreground/25 shadow-xl"
      :style="getCircleStyle(i - 1)" />
  </div>
</template>

<script setup lang="ts">
interface RippleProps {
  mainCircleSize?: number;
  mainCircleOpacity?: number;
  numCircles?: number;
}

const props = defineProps<RippleProps>();

const mainCircleSize = props.mainCircleSize ?? 350;
const mainCircleOpacity = props.mainCircleOpacity ?? 0.2;
const numCircles = props.numCircles ?? 8;

const getCircleStyle = (i: number) => {
  const size = mainCircleSize + i * 70;
  const opacity = mainCircleOpacity - i * 0.03;
  const animationDelay = `${i * 0.06}s`;
  const borderStyle = i === numCircles - 1 ? "dashed" : "solid";
  const borderOpacity = 5 + i * 5;

  return {
    width: `${size}px`,
    height: `${size}px`,
    opacity: opacity,
    animationDelay: animationDelay,
    borderStyle: borderStyle,
    borderRadius: "9999px",
    borderWidth: "1px",
    borderColor: `rgba(var(--foreground-rgb), ${borderOpacity / 100})`,
    transform: 'translate(-50%, -50%)',
    position: "absolute"
  };
};
</script>

<style scoped>
@keyframes ripple {

  0%,
  100% {
    transform: translate(-50%, -50%) scale(1);
    /* opacity: 0; */
  }

  50% {
    transform: translate(-50%, -50%) scale(0.8);
    /* opacity: 0.7; */
  }

  /* 0% {
    transform: translate(-50%, -50%) scale(0.8);
  }

  100% {
    transform: translate(-50%, -50%) scale(3.5);
    opacity: 0;
  } */
}

.animate-ripple {
  animation: ripple 3s infinite;
}
</style>
