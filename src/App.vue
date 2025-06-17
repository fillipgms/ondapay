<script setup>
import {
  PhCheckCircle,
  PhCurrencyDollar,
  PhLightning,
  PhStackPlus,
  PhThumbsUp,
  PhUsersThree,
} from '@phosphor-icons/vue'
import SpotlightEffect from './components/spotlight.vue'
import FaqItem from './components/FaqItem.vue'
</script>

<template>
  <main class="bg-gradient-to-b bg-background relative text-foreground dark">
    <div class="fixed inset-0 pointer-events-none overflow-hidden">
      <div
        class="absolute w-72 h-72 bg-primary/10 rounded-full blur-[96px] animate-float-slow"
      ></div>
      <div
        class="absolute w-72 h-72 bg-primary/10 rounded-full blur-[96px] animate-float-reverse"
      ></div>
      <div
        class="absolute w-72 h-72 bg-primary/10 rounded-full blur-[96px] animate-float-delayed"
      ></div>
    </div>

    <section
      class="flex flex-col items-center container mx-auto gap-8 min-h-svh py-16 px-4 md:py-24 relative overflow-hidden"
    >
      <h1
        class="md:text-7xl text-center text-5xl font-bold font-quanta-grotesk-pro max-w-2xl leading-tight relative"
      >
        Tome o
        <span class="text-primary relative">
          Controle
          <span class="absolute inset-0"></span>
        </span>
        da sua carteira digital
      </h1>
      <p class="max-w-xl text-lg text-gray-300 text-center">
        Pagamentos seguros, rápidos e sem complicação. OndaPay é a solução para quem quer agilidade
        e integração fácil.
      </p>
      <div class="flex gap-4 justify-center">
        <button
          class="bg-primary hover:bg-primary/90 transition-all duration-300 cursor-pointer text-background px-8 py-4 rounded-xl font-semibold shadow-lg hover:shadow-xl hover:-translate-y-0.5 group relative overflow-hidden"
        >
          <span class="relative z-10">Quero Experimentar</span>
          <div
            class="absolute inset-0 bg-gradient-to-r from-primary/0 via-white/20 to-primary/0 translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-1000"
          ></div>
        </button>
      </div>

      <div
        class="relative z-10 mt-20 rounded-3xl border border-primary/10 bg-background-secondary/90 backdrop-blur-lg p-4 shadow-md hover:shadow-lg transition-all duration-300"
      >
        <div class="w-full overflow-hidden rounded-xl border border-primary/10">
          <img
            alt="Landing page preview"
            class="aspect-[16/9] h-auto w-full object-cover"
            height="1000"
            width="1000"
            src="./assets/preview.jpg"
          />
        </div>
      </div>
    </section>

    <section class="py-16 md:py-24 space-y-12 px-4 relative">
      <div
        class="absolute inset-0 bg-gradient-to-b from-background/0 via-primary/5 to-background/0"
      ></div>
      <h2
        class="text-center text-4xl md:text-5xl font-bold font-quanta-grotesk-pro max-w-3xl mx-auto relative"
      >
        Por que escolher a
        <span class="text-primary relative">
          OndaPay
          <span class="absolute inset-0"></span>
        </span>
      </h2>

      <div class="container mx-auto relative">
        <div
          class="bg-background-secondary/90 backdrop-blur-lg rounded-2xl p-6 md:p-8 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8 border border-primary/10 transition-all duration-300"
        >
          <div class="flex flex-col gap-3 p-4 rounded-lg transition-all duration-300 group">
            <div class="flex items-center gap-3">
              <div class="p-2 rounded-lg bg-primary/10 transition-colors">
                <PhLightning size="28" class="text-primary" />
              </div>
              <h3 class="text-xl md:text-2xl font-bold font-quanta-grotesk-pro">Agilidade</h3>
            </div>
            <p class="text-sm md:text-base text-gray-300">
              PIX gerados e transferidos em segundos.
            </p>
          </div>
          <div class="flex flex-col gap-3 p-4 rounded-lg transition-all duration-300 group">
            <div class="flex items-center gap-3">
              <div class="p-2 rounded-lg bg-primary/10 transition-colors">
                <PhStackPlus size="28" class="text-primary" />
              </div>
              <h3 class="text-xl md:text-2xl font-bold font-quanta-grotesk-pro">Escalabilidade</h3>
            </div>
            <p class="text-sm md:text-base text-gray-300">Pronto para crescer junto com você.</p>
          </div>
          <div class="flex flex-col gap-3 p-4 rounded-lg transition-all duration-300 group">
            <div class="flex items-center gap-3">
              <div class="p-2 rounded-lg bg-primary/10 transition-colors">
                <PhCheckCircle size="28" class="text-primary" />
              </div>
              <h3 class="text-xl md:text-2xl font-bold font-quanta-grotesk-pro">Segurança</h3>
            </div>
            <p class="text-sm md:text-base text-gray-300">
              Certificação PCI DSS e criptografia ponta a ponta.
            </p>
          </div>
          <div class="flex flex-col gap-3 p-4 rounded-lg transition-all duration-300 group">
            <div class="flex items-center gap-3">
              <div class="p-2 rounded-lg bg-primary/10 transition-colors">
                <PhCurrencyDollar size="28" class="text-primary" />
              </div>
              <h3 class="text-xl md:text-2xl font-bold font-quanta-grotesk-pro">Baixas taxas</h3>
            </div>
            <p class="text-sm md:text-base text-gray-300">Mais economia para você ou seu app.</p>
          </div>

          <div class="flex flex-col gap-3 p-4 rounded-lg transition-all duration-300 group">
            <div class="flex items-center gap-3">
              <div class="p-2 rounded-lg bg-primary/10 transition-colors">
                <PhUsersThree size="28" class="text-primary" />
              </div>
              <h3 class="text-xl md:text-2xl font-bold font-quanta-grotesk-pro">Para Todos</h3>
            </div>
            <p class="text-sm md:text-base text-gray-300">
              Fluxo simples, pensado para todos os públicos.
            </p>
          </div>

          <div class="flex flex-col gap-3 p-4 rounded-lg transition-all duration-300 group">
            <div class="flex items-center gap-3">
              <div class="p-2 rounded-lg bg-primary/10 transition-colors">
                <PhThumbsUp size="28" class="text-primary" />
              </div>
              <h3 class="text-xl md:text-2xl font-bold font-quanta-grotesk-pro">Confiável</h3>
            </div>
            <p class="text-sm md:text-base text-gray-300">+1.000 pessoas já usam OndaPay.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="py-16 md:py-24">
      <div class="container mx-auto grid grid-cols-1 md:grid-cols-3 gap-8 items-center">
        <div
          class="bg-primary text-background rounded-3xl p-8 flex flex-col items-center justify-center h-full relative overflow-hidden group hover:shadow-lg transition-all duration-300"
        >
          <div
            class="absolute inset-0 bg-gradient-to-r from-primary/0 via-white/5 to-primary/0 translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-1000"
          ></div>
          <h3 class="text-xl font-bold mb-2">Sem taxas escondidas</h3>
          <p class="text-center">
            Transparência total para você focar no que importa: seu dinheiro.
          </p>
        </div>

        <div
          class="md:col-span-2 bg-background-secondary/90 backdrop-blur-lg rounded-3xl p-8 flex flex-col gap-6 shadow-lg relative hover:shadow-xl transition-all duration-300"
        >
          <h2 class="text-3xl md:text-4xl font-bold font-quanta-grotesk-pro mb-2">
            Seu Financeiro <span class="text-primary">Como Nunca Antes</span>
          </h2>
          <p class="text-gray-300 mb-4">
            Saque instantâneo via Pix, integração fácil e taxas baixas. Tudo isso com a segurança e
            agilidade que só a OndaPay oferece.
          </p>
          <button
            class="bg-primary w-fit hover:bg-primary/90 transition-all duration-300 cursor-pointer text-background px-8 py-4 rounded-xl font-semibold shadow-lg hover:shadow-xl hover:-translate-y-0.5 group relative overflow-hidden"
          >
            <span class="relative z-10">Quero Experimentar</span>
            <div
              class="absolute inset-0 bg-gradient-to-r from-primary/0 via-white/20 to-primary/0 translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-1000"
            ></div>
          </button>

          <div class="absolute -top-8 -right-8 w-24 h-24 bg-primary/10 rounded-full blur-2xl"></div>
        </div>
      </div>
    </section>

    <section class="py-16 md:py-24">
      <div class="container mx-auto grid grid-cols-1 md:grid-cols-3 gap-12 relative">
        <h2 class="text-4xl md:text-5xl font-bold font-quanta-grotesk-pro leading-tight">
          Quem Já Usa,
          <span class="text-primary relative inline-block">
            Adora
            <span class="absolute inset-0"></span>
          </span>
        </h2>

        <div
          class="flex flex-col justify-between order-3 md:order-2 bg-background-secondary/90 backdrop-blur-lg p-8 rounded-2xl border border-primary/10 transition-all duration-300"
        >
          <p class="text-lg text-gray-300">
            "A OndaPay era exatamente o que eu precisava. Agora, eu consigo fazer todas as minhas
            transações em um lugar só. É como se alguém tivesse feito um sistema de pagamentos
            pensando em mim."
          </p>

          <h3 class="flex flex-col mt-6">
            <span class="text-primary font-bold text-lg">Maria da Silva</span>
            <span class="text-gray-300">CEO da OndaPay</span>
          </h3>
        </div>

        <div class="order-2 md:order-3 relative group">
          <img
            src="./assets/testimonial.jpg"
            alt="Maria da Silva"
            class="w-full aspect-square object-cover rounded-2xl scale-x-[-1] relative z-10 duration-500"
          />
          <div class="absolute inset-0 bg-primary/10 rounded-2xl blur-lg -z-10"></div>
        </div>
      </div>
    </section>

    <section class="py-16 md:py-24">
      <div class="container mx-auto">
        <div
          class="bg-primary rounded-[2rem] text-background p-8 md:p-12 shadow-lg relative overflow-hidden group hover:shadow-xl transition-all duration-300"
        >
          <div
            class="absolute inset-0 bg-gradient-to-r from-primary/0 via-white/5 to-primary/0 translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-1000"
          ></div>
          <h2 class="text-background text-2xl md:text-3xl font-bold mb-10 text-center">
            Passos para Integração
          </h2>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-2">
            <div class="flex md:flex-col gap-2">
              <div class="flex md:flex-row flex-col items-center gap-2 md:w-full">
                <div class="w-4 h-4 aspect-square rounded-full bg-background"></div>
                <div
                  class="md:w-full md:h-px h-full w-px border border-dashed border-background"
                ></div>
              </div>
              <div class="flex flex-col gap-2">
                <span class="font-bold text-lg">Crie sua conta</span>
                <span class="text-sm">Crie sua conta em menos de um minuto</span>
              </div>
            </div>

            <div class="flex md:flex-col gap-2">
              <div class="flex md:flex-row flex-col items-center gap-2 md:w-full">
                <div class="w-4 h-4 aspect-square rounded-full bg-background"></div>
                <div
                  class="md:w-full md:h-px h-full w-px border border-dashed border-background"
                ></div>
              </div>
              <div class="flex flex-col gap-2">
                <span class="font-bold text-lg">Adicione seu banco</span>
                <span class="text-sm"
                  >Segurança de ponta a ponta para você conectar sua conta do banco</span
                >
              </div>
            </div>

            <div class="flex md:flex-col gap-2">
              <div class="flex md:flex-row flex-col items-center gap-2 md:w-full">
                <div class="w-4 h-4 aspect-square rounded-full bg-background"></div>
                <div
                  class="md:w-full md:h-px h-full w-px border border-dashed border-background"
                ></div>
              </div>
              <div class="flex flex-col gap-2">
                <span class="font-bold text-lg">Comece a usar</span>
                <span class="text-sm">Envie, receba e organize seu dinheiro</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="py-16 md:py-24">
      <div class="container mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">
        <div>
          <h2 class="text-4xl font-bold font-quanta-grotesk-pro leading-tight">
            Tem Dúvidas?
            <span class="text-primary relative">
              Vamos te ajudar!
              <span class="absolute inset-0"></span>
            </span>
          </h2>
        </div>
        <div class="md:col-span-2 space-y-4">
          <FaqItem question="O que é a OndaPay?">
            A OndaPay é uma plataforma de pagamentos digitais focada em agilidade, segurança e
            integração fácil. Com ela, você gera e envia Pix de forma instantânea, com taxas baixas
            e total controle sobre suas transações.
          </FaqItem>

          <FaqItem question="Preciso conectar todas as minhas contas bancárias para usar?">
            Não! Você pode começar com apenas uma conta. A conexão de múltiplas contas é opcional e
            serve apenas para te dar mais flexibilidade e controle centralizado dos seus
            recebimentos e envios.
          </FaqItem>

          <FaqItem question="A OndaPay funciona com qualquer banco?">
            Sim. Os saques e recebimentos são feitos via Pix, então você pode transferir para
            qualquer banco ou fintech compatível com o sistema de pagamentos instantâneos do Brasil.
          </FaqItem>

          <FaqItem question="A plataforma é segura mesmo?">
            Com certeza. A OndaPay utiliza criptografia ponta a ponta, além de seguir padrões de
            segurança como a certificação PCI DSS. Seus dados e transações estão protegidos do
            início ao fim.
          </FaqItem>

          <FaqItem question="Sou desenvolvedor. Consigo integrar a OndaPay no meu sistema?">
            Sim! Temos uma API simples e bem documentada, perfeita pra quem quer integrar geração e
            envio de Pix direto em sistemas próprios — seja uma loja, app ou plataforma de gestão.
          </FaqItem>

          <FaqItem question="Preciso ser empresa pra usar a OndaPay?">
            Não. Qualquer pessoa física ou jurídica pode usar. A gente quer facilitar a vida de quem
            vende, recebe ou transfere, sem burocracia.
          </FaqItem>
        </div>
      </div>
    </section>

    <footer
      class="bg-background-secondary/90 backdrop-blur-lg text-foreground py-12 rounded-t-3xl space-y-12 relative"
    >
      <section>
        <div class="container mx-auto relative">
          <div
            class="bg-gradient-to-br from-primary to-primary/80 text-background rounded-3xl p-8 md:p-12 relative overflow-hidden"
          >
            <div class="absolute inset-0 z-0">
              <SpotlightEffect
                :gradient-first="'radial-gradient(68.54% 68.72% at 55.02% 31.46%, hsla(140, 80%, 85%, 0.12) 0, hsla(140, 54%, 80%, 0.08) 50%, hsla(140, 77%, 90%, 0.06) 100%)'"
                :gradient-second="'radial-gradient(50% 50% at 50% 50%, hsla(140, 77%, 90%, 0.06) 0, hsla(140, 80%, 85%, 0.04) 80%, transparent 100%)'"
                :gradient-third="'radial-gradient(50% 50% at 50% 50%, hsla(140, 54%, 80%, 0.06) 0, hsla(140, 80%, 85%, 0.03) 80%, transparent 100%)'"
                :translate-y="-250"
                :width="800"
                :height="1600"
                :small-width="400"
                :duration="12"
                :x-offset="120"
              />
            </div>
            <div class="relative z-10 space-y-6">
              <h2
                class="text-4xl md:text-5xl text-center capitalize lg:text-6xl font-bold font-quanta-grotesk-pro leading-tight"
              >
                Pronto Pra surfar <br class="hidden md:block" />
                <span class="relative inline-block"> Nessa onda? </span>
              </h2>

              <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <button
                  class="bg-background hover:bg-background/90 transition-all duration-300 cursor-pointer text-primary px-8 py-4 rounded-xl font-semibold shadow-lg hover:shadow-xl hover:-translate-y-0.5 group relative overflow-hidden"
                >
                  <span class="relative z-10">Começar Agora</span>
                  <div
                    class="absolute inset-0 bg-gradient-to-r from-background/0 via-white/20 to-background/0 translate-x-[-100%] group-hover:translate-x-[100%] transition-transform duration-1000"
                  ></div>
                </button>
              </div>
            </div>
          </div>
        </div>
      </section>

      <div class="container mx-auto px-4 relative z-10">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
          <div class="space-y-4 col-span-1 md:col-span-2">
            <h3 class="text-2xl font-bold font-quanta-grotesk-pro">OndaPay</h3>
            <p class="text-sm text-gray-300">Sua solução completa para pagamentos digitais.</p>
          </div>

          <div class="space-y-4">
            <h4 class="font-semibold text-lg">Produto</h4>
            <ul class="space-y-2 text-sm text-gray-300">
              <li><a href="#" class="hover:text-primary transition-colors">Recursos</a></li>
              <li><a href="#" class="hover:text-primary transition-colors">Preços</a></li>
              <li><a href="#" class="hover:text-primary transition-colors">Integrações</a></li>
            </ul>
          </div>

          <div class="space-y-4">
            <h4 class="font-semibold text-lg">Legal</h4>
            <ul class="space-y-2 text-sm text-gray-300">
              <li><a href="#" class="hover:text-primary transition-colors">Termos</a></li>
              <li><a href="#" class="hover:text-primary transition-colors">Privacidade</a></li>
              <li><a href="#" class="hover:text-primary transition-colors">Segurança</a></li>
            </ul>
          </div>
        </div>

        <div
          class="mt-12 pt-8 border-t border-gray-700/50 flex flex-col md:flex-row justify-between items-center gap-4"
        >
          <p class="text-sm text-gray-300">© 2025 OndaPay. Todos os direitos reservados.</p>
          <div class="flex gap-4">
            <a href="#" class="text-gray-300 hover:text-primary transition-colors">
              <i class="fab fa-twitter text-xl"></i>
            </a>
            <a href="#" class="text-gray-300 hover:text-primary transition-colors">
              <i class="fab fa-linkedin text-xl"></i>
            </a>
            <a href="#" class="text-gray-300 hover:text-primary transition-colors">
              <i class="fab fa-instagram text-xl"></i>
            </a>
          </div>
        </div>
      </div>
    </footer>
  </main>
</template>

<style>
@keyframes float-slow {
  0% {
    transform: translate(0, 0);
  }
  25% {
    transform: translate(100px, 50px);
  }
  50% {
    transform: translate(50px, 100px);
  }
  75% {
    transform: translate(-50px, 50px);
  }
  100% {
    transform: translate(0, 0);
  }
}

@keyframes float-reverse {
  0% {
    transform: translate(0, 0);
  }
  25% {
    transform: translate(-100px, -50px);
  }
  50% {
    transform: translate(-50px, -100px);
  }
  75% {
    transform: translate(50px, -50px);
  }
  100% {
    transform: translate(0, 0);
  }
}

@keyframes float-delayed {
  0% {
    transform: translate(0, 0);
  }
  25% {
    transform: translate(50px, -100px);
  }
  50% {
    transform: translate(-100px, -50px);
  }
  75% {
    transform: translate(-50px, 100px);
  }
  100% {
    transform: translate(0, 0);
  }
}

.animate-float-slow {
  animation: float-slow 20s ease-in-out infinite;
  top: 20%;
  left: 20%;
}

.animate-float-reverse {
  animation: float-reverse 25s ease-in-out infinite;
  top: 60%;
  left: 60%;
}

.animate-float-delayed {
  animation: float-delayed 30s ease-in-out infinite;
  top: 40%;
  left: 40%;
}

@keyframes float {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-5px);
  }
}

.animate-float {
  animation: float 4s ease-in-out infinite;
}

@keyframes glow {
  0%,
  100% {
    opacity: 0.3;
  }
  50% {
    opacity: 0.5;
  }
}

.animate-glow {
  animation: glow 3s ease-in-out infinite;
}
</style>
