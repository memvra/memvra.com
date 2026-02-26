<script setup>
import { ref } from 'vue'

const copied = ref(false)

function copyInstall() {
  navigator.clipboard.writeText('brew install memvra/tap/memvra')
  copied.value = true
  setTimeout(() => { copied.value = false }, 2000)
}
</script>

<template>
  <section class="relative overflow-hidden px-6 pt-24 pb-20 sm:pt-32 sm:pb-28">
    <!-- Background gradient -->
    <div class="absolute inset-0 -z-10">
      <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-primary/10 rounded-full blur-[128px]"></div>
      <div class="absolute top-1/3 left-1/3 w-[400px] h-[400px] bg-accent/8 rounded-full blur-[100px]"></div>
    </div>

    <div class="mx-auto max-w-4xl text-center">
      <!-- Badge -->
      <div class="fade-in inline-flex items-center gap-2 rounded-full border border-border px-4 py-1.5 text-sm text-text-muted mb-8">
        <span class="inline-block w-2 h-2 rounded-full bg-green-400"></span>
        Open source &middot; Local-first &middot; MIT License
      </div>

      <!-- Headline -->
      <h1 class="fade-in fade-in-delay-1 text-4xl sm:text-6xl lg:text-7xl font-bold tracking-tight leading-[1.1] mb-6">
        Your AI finally<br />
        <span class="gradient-text">remembers your project.</span>
      </h1>

      <!-- Subline -->
      <p class="fade-in fade-in-delay-2 text-lg sm:text-xl text-text-muted max-w-2xl mx-auto mb-10">
        Persistent Memory &middot; Vector Intelligence &middot; One CLI<br class="hidden sm:block" />
        Switch between Claude, Gemini, Cursor &mdash; type <code class="text-primary font-mono text-base">"continue"</code> and it picks up where you left off.
      </p>

      <!-- Install command -->
      <div class="fade-in fade-in-delay-3 flex flex-col sm:flex-row items-center justify-center gap-4 mb-8">
        <div
          @click="copyInstall"
          class="group flex items-center gap-3 bg-surface-light border border-border rounded-lg px-5 py-3 font-mono text-sm cursor-pointer hover:border-primary/50 transition-colors"
        >
          <span class="text-text-muted">$</span>
          <span class="text-white">brew install memvra/tap/memvra</span>
          <span class="text-text-muted group-hover:text-primary transition-colors">
            {{ copied ? '\u2713' : '\u2398' }}
          </span>
        </div>
      </div>

      <!-- CTA buttons -->
      <div class="fade-in fade-in-delay-4 flex flex-col sm:flex-row items-center justify-center gap-4">
        <a
          href="https://github.com/memvra/memvra"
          target="_blank"
          class="inline-flex items-center gap-2 bg-primary hover:bg-primary-dark text-white font-semibold rounded-lg px-6 py-3 transition-colors"
        >
          <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
          View on GitHub
        </a>
        <a
          href="#install"
          class="inline-flex items-center gap-2 border border-border hover:border-primary/50 text-white font-semibold rounded-lg px-6 py-3 transition-colors"
        >
          Get Started
        </a>
      </div>
    </div>
  </section>
</template>
