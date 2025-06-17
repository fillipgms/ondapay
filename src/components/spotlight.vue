<script setup>
import { ref, onMounted } from 'vue'

defineOptions({
  name: 'SpotlightEffect',
})

const props = defineProps({
  gradientFirst: {
    type: String,
    default:
      'radial-gradient(68.54% 68.72% at 55.02% 31.46%, hsla(210, 100%, 85%, .08) 0, hsla(210, 100%, 55%, .02) 50%, hsla(210, 100%, 45%, 0) 80%)',
  },
  gradientSecond: {
    type: String,
    default:
      'radial-gradient(50% 50% at 50% 50%, hsla(210, 100%, 85%, .06) 0, hsla(210, 100%, 55%, .02) 80%, transparent 100%)',
  },
  gradientThird: {
    type: String,
    default:
      'radial-gradient(50% 50% at 50% 50%, hsla(210, 100%, 85%, .04) 0, hsla(210, 100%, 45%, .02) 80%, transparent 100%)',
  },
  translateY: {
    type: Number,
    default: -350,
  },
  width: {
    type: Number,
    default: 560,
  },
  height: {
    type: Number,
    default: 1380,
  },
  smallWidth: {
    type: Number,
    default: 240,
  },
  duration: {
    type: Number,
    default: 7,
  },
  xOffset: {
    type: Number,
    default: 100,
  },
})

const leftX = ref(0)
const leftY = ref(0)
const rightX = ref(0)
const rightY = ref(0)
const opacity = ref(0)

onMounted(() => {
  // Fade in animation
  opacity.value = 1

  // Continuous movement animation
  const animate = () => {
    const timestamp = Date.now()
    const progress = (timestamp % (props.duration * 1000)) / (props.duration * 1000)

    // Organic, wavy movement
    leftX.value = Math.sin(progress * Math.PI * 2) * props.xOffset
    leftY.value = Math.cos(progress * Math.PI * 2) * (props.xOffset * 0.4)
    rightX.value = -Math.sin(progress * Math.PI * 2 + Math.PI / 3) * props.xOffset
    rightY.value = Math.cos(progress * Math.PI * 2 + Math.PI / 2) * (props.xOffset * 0.4)

    requestAnimationFrame(animate)
  }

  requestAnimationFrame(animate)
})
</script>

<template>
  <div style="filter: blur(10px); pointer-events: none">
    <div class="pointer-events-none absolute inset-0 h-full w-full" :style="{ opacity }">
      <!-- Left side gradients -->
      <div
        class="absolute top-0 left-0 w-screen h-screen z-0 pointer-events-none"
        :style="{ transform: `translateX(${leftX}px) translateY(${leftY}px)` }"
      >
        <div
          :style="{
            transform: `translateY(${translateY}px) rotate(-45deg)`,
            background: gradientFirst,
            width: `${width}px`,
            height: `${height}px`,
          }"
          class="absolute top-0 left-0"
        />

        <div
          :style="{
            transform: 'rotate(-45deg) translate(5%, -50%)',
            background: gradientSecond,
            width: `${smallWidth}px`,
            height: `${height}px`,
          }"
          class="absolute top-0 left-0 origin-top-left"
        />

        <div
          :style="{
            transform: 'rotate(-45deg) translate(-180%, -70%)',
            background: gradientThird,
            width: `${smallWidth}px`,
            height: `${height}px`,
          }"
          class="absolute top-0 left-0 origin-top-left"
        />
      </div>

      <!-- Right side gradients -->
      <div
        class="absolute top-0 right-0 w-screen h-screen z-0 pointer-events-none"
        :style="{ transform: `translateX(${rightX}px) translateY(${rightY}px)` }"
      >
        <div
          :style="{
            transform: `translateY(${translateY}px) rotate(45deg)`,
            background: gradientFirst,
            width: `${width}px`,
            height: `${height}px`,
          }"
          class="absolute top-0 right-0"
        />

        <div
          :style="{
            transform: 'rotate(45deg) translate(-5%, -50%)',
            background: gradientSecond,
            width: `${smallWidth}px`,
            height: `${height}px`,
          }"
          class="absolute top-0 right-0 origin-top-right"
        />

        <div
          :style="{
            transform: 'rotate(45deg) translate(180%, -70%)',
            background: gradientThird,
            width: `${smallWidth}px`,
            height: `${height}px`,
          }"
          class="absolute top-0 right-0 origin-top-right"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.pointer-events-none {
  pointer-events: none;
}
</style>
