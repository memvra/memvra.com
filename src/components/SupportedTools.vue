<template>
  <section class="px-6 py-20 sm:py-28">
    <div class="mx-auto max-w-4xl text-center">
      <h2 class="text-3xl sm:text-4xl font-bold mb-4">
        Works with <span class="gradient-text">every AI tool</span>
      </h2>
      <p class="text-text-muted text-lg mb-16 max-w-2xl mx-auto">
        MCP-native integration for IDEs. Transparent wrapping for CLI tools.
      </p>

      <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-6 gap-4 mb-12">
        <div
          v-for="tool in tools"
          :key="tool.name"
          class="flex flex-col items-center gap-3 rounded-xl border border-border bg-surface-light p-5 hover:border-primary/30 transition-colors"
        >
          <div class="text-2xl font-bold" :style="{ color: tool.color }">{{ tool.icon }}</div>
          <span class="text-sm font-medium">{{ tool.name }}</span>
          <span class="text-xs text-text-muted">{{ tool.type }}</span>
        </div>
      </div>

      <!-- Integration types -->
      <div class="grid sm:grid-cols-3 gap-4 text-left">
        <div class="rounded-lg border border-border bg-surface-light p-4">
          <div class="text-primary text-sm font-semibold mb-2">MCP Server</div>
          <p class="text-text-muted text-xs leading-relaxed">
            Claude Code, Cursor, and Windsurf call Memvra tools automatically. Zero manual steps.
          </p>
          <code class="text-xs text-primary/70 mt-2 block">memvra mcp install</code>
        </div>
        <div class="rounded-lg border border-border bg-surface-light p-4">
          <div class="text-accent text-sm font-semibold mb-2">Wrap</div>
          <p class="text-text-muted text-xs leading-relaxed">
            Launch any CLI tool with context injected. Session captured on exit.
          </p>
          <code class="text-xs text-accent/70 mt-2 block">memvra wrap gemini</code>
        </div>
        <div class="rounded-lg border border-border bg-surface-light p-4">
          <div class="text-green-400 text-sm font-semibold mb-2">Auto-Export</div>
          <p class="text-text-muted text-xs leading-relaxed">
            Context files in every format — updated automatically on every change.
          </p>
          <code class="text-xs text-green-400/70 mt-2 block">CLAUDE.md, .cursorrules, ...</code>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const tools = [
  { name: "Claude Code", icon: "C", color: "#d97706", type: "MCP" },
  { name: "Cursor", icon: "Cu", color: "#8b5cf6", type: "MCP" },
  { name: "Windsurf", icon: "W", color: "#06b6d4", type: "MCP" },
  { name: "Gemini", icon: "G", color: "#4285f4", type: "Wrap" },
  { name: "Aider", icon: "A", color: "#22c55e", type: "Wrap" },
  { name: "Ollama", icon: "O", color: "#f5f5f5", type: "Wrap" },
]
</script>
