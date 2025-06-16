<template>
  <div class="relative">
    <div
      class="absolute top-0 -translate-y-1/2 p-4 right-0 z-10 bg-primary text-background rounded-2xl flex flex-col items-center justify-center"
    >
      <div class="flex items-center gap-2">
        <PhCheckCircle class="text-background" />
        <p class="font-bold">Transferência bem-sucedida</p>
      </div>
    </div>

    <div
      class="bg-background-secondary w-full max-w-md mx-auto rounded-2xl flex flex-col border border-primary/10 p-8 text-foreground gap-6 shadow-lg relative"
    >
      <h3 class="text-2xl font-bold mb-2">Transferência</h3>

      <!-- Valores enviados e recebidos -->
      <div class="flex flex-col gap-4">
        <div class="flex items-center justify-between bg-primary/5 rounded-lg p-4">
          <div class="flex items-center gap-2">
            <PhArrowsLeftRight class="text-primary" />
            <span class="font-medium">Você enviou</span>
          </div>
          <div class="flex items-center gap-2">
            <span class="text-lg font-bold">R$ 1.000,00</span>
          </div>
        </div>
        <div class="flex items-center justify-between bg-primary/5 rounded-lg p-4">
          <div class="flex items-center gap-2">
            <PhArrowsLeftRight class="text-primary" />
            <span class="font-medium">Destinatário recebe</span>
          </div>
          <div class="flex items-center gap-2">
            <span class="text-lg font-bold">$ 1,136.85</span>
          </div>
        </div>
      </div>

      <!-- Informações adicionais -->
      <div class="flex flex-col gap-2 text-sm mt-2">
        <div class="flex items-center justify-between">
          <span class="flex items-center gap-1">
            <PhLightning class="text-primary" size="18" />
            Chegada estimada
          </span>
          <span class="font-semibold">Agora</span>
        </div>
      </div>

      <!-- Botão de ação -->
      <button
        class="mt-6 bg-primary hover:bg-primary/90 transition-all duration-300 cursor-pointer text-background px-8 py-4 rounded-xl font-semibold shadow-lg hover:shadow-xl hover:-translate-y-0.5 group relative overflow-hidden w-full text-lg"
      >
        <span class="relative z-10">Enviar Agora</span>
        <div
          class="absolute inset-0 bg-gradient-to-r from-primary/0 via-white/20 to-primary/0 translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-1000"
        ></div>
      </button>
    </div>
  </div>
</template>

<script setup>
import { PhArrowsLeftRight, PhLightning, PhCheckCircle } from '@phosphor-icons/vue'
</script>

<style scoped></style>
