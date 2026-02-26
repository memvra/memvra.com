<script setup>
import { ref } from 'vue'

const activeTab = ref('brew')
const copied = ref(false)

const commands = {
  brew: 'brew install memvra/tap/memvra',
  curl: 'curl -fsSL https://memvra.com/install.sh | sh',
  go: 'go install github.com/memvra/memvra@latest'
}

function copy() {
  navigator.clipboard.writeText(commands[activeTab.value])
  copied.value = true
  setTimeout(() => { copied.value = false }, 2000)
}
</script>

<template>
  <section id="install" class="px-6 py-20 sm:py-28 bg-surface/50">
    <div class="mx-auto max-w-3xl">
      <h2 class="text-3xl sm:text-4xl font-bold text-center mb-4">
        Get started in <span class="gradient-text">30 seconds</span>
      </h2>
      <p class="text-text-muted text-center text-lg mb-12">
        Install Memvra, initialize your project, and your AI tools gain persistent memory.
      </p>

      <!-- Tabs -->
      <div class="flex justify-center gap-2 mb-6">
        <button
          v-for="tab in ['brew', 'curl', 'go']"
          :key="tab"
          @click="activeTab = tab"
          :class="[
            'px-4 py-2 rounded-lg text-sm font-medium transition-colors',
            activeTab === tab
              ? 'bg-primary/20 text-primary border border-primary/30'
              : 'text-text-muted hover:text-white border border-transparent'
          ]"
        >
          {{ tab === 'brew' ? 'Homebrew' : tab === 'curl' ? 'curl' : 'Go install' }}
        </button>
      </div>

      <!-- Command -->
      <div
        @click="copy"
        class="group flex items-center justify-between bg-surface-light border border-border rounded-xl px-6 py-4 font-mono text-sm cursor-pointer hover:border-primary/30 transition-colors mb-8"
      >
        <div>
          <span class="text-text-muted">$ </span>
          <span class="text-white">{{ commands[activeTab] }}</span>
        </div>
        <span class="text-text-muted group-hover:text-primary transition-colors text-xs ml-4 shrink-0">
          {{ copied ? 'Copied!' : 'Click to copy' }}
        </span>
      </div>

      <!-- Quick start -->
      <div class="bg-surface-light border border-border rounded-xl p-6 font-mono text-sm">
        <p class="text-text-muted mb-3"># Quick start</p>
        <p class="mb-1"><span class="text-text-muted">$ </span><span class="text-white">cd your-project/</span></p>
        <p class="mb-1"><span class="text-text-muted">$ </span><span class="text-white">memvra init</span></p>
        <p class="text-green-400 text-xs mb-3">&#10003; Scanned 142 files, 1,847 chunks, 12 memories stored</p>
        <p class="mb-1"><span class="text-text-muted">$ </span><span class="text-white">memvra remember "Use JWT auth with RS256, tokens expire in 1h"</span></p>
        <p class="text-green-400 text-xs mb-3">&#10003; Stored as: decision — auto-exported to CLAUDE.md, .cursorrules</p>
        <p class="mb-1"><span class="text-text-muted">$ </span><span class="text-white">memvra ask "How should I implement the auth middleware?"</span></p>
        <p class="text-primary text-xs">&#8594; Full project context injected automatically</p>
      </div>

      <!-- Docs link -->
      <p class="text-center text-text-muted text-sm mt-8">
        Full documentation on
        <a href="https://github.com/memvra/memvra#readme" target="_blank" class="text-primary hover:underline">GitHub</a>
      </p>
    </div>
  </section>
</template>
