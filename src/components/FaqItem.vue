<template>
  <div class="pb-4 cursor-pointer" @click="toggle">
    <button
      class="w-full cursor-pointer flex justify-between items-center text-left focus:outline-none group"
    >
      <span class="font-bold text-xl text-foreground transition">
        {{ question }}
      </span>
      <PhPlus weight="bold" v-if="!open" class="text-xl transition-transform duration-300" />
      <PhMinus weight="bold" v-else class="text-xl transition-transform duration-300" />
    </button>

    <div
      v-show="open"
      ref="content"
      class="text-gray-300 overflow-hidden transition-all duration-500 ease-in-out"
      :style="{ maxHeight: open ? contentHeight + 'px' : '0' }"
    >
      <div ref="inner" class="pt-4 leading-relaxed tracking-wide">
        <slot />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, nextTick } from 'vue'
import { PhPlus, PhMinus } from '@phosphor-icons/vue'

const open = ref(false)
const content = ref(null)
const inner = ref(null)
const contentHeight = ref(0)

const toggle = async () => {
  open.value = !open.value
  await nextTick()
  contentHeight.value = inner.value.scrollHeight
}

defineProps(['question'])
</script>

<style scoped>
.slide-fade-enter-active,
.slide-fade-leave-active {
  transition: all 0.3s ease;
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  opacity: 0;
  transform: translateY(-5px);
}

.slide-fade-enter-to,
.slide-fade-leave-from {
  opacity: 1;
  transform: translateY(0);
}
</style>
