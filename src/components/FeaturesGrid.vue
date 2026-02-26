<template>
  <section class="px-6 py-20 sm:py-28 bg-surface/50">
    <div class="mx-auto max-w-6xl">
      <h2 class="text-3xl sm:text-4xl font-bold text-center mb-4">
        Everything your AI <span class="gradient-text">needs to remember</span>
      </h2>
      <p class="text-text-muted text-center text-lg mb-16 max-w-2xl mx-auto">
        One CLI. Every AI tool. Zero cloud dependency.
      </p>

      <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="feature in features"
          :key="feature.title"
          class="rounded-xl border border-border bg-surface-light p-6 hover:border-primary/30 transition-colors"
        >
          <div class="text-3xl mb-4">{{ feature.icon }}</div>
          <h3 class="text-lg font-semibold mb-2">{{ feature.title }}</h3>
          <p class="text-text-muted text-sm leading-relaxed">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    icon: "\u{1F9E0}",
    title: "Persistent Memory",
    description: "Decisions, conventions, constraints, and notes survive across sessions. Store once, use everywhere."
  },
  {
    icon: "\u{1F50D}",
    title: "Vector Search",
    description: "Semantic retrieval using embeddings. Ask a question and Memvra finds the most relevant code and memories."
  },
  {
    icon: "\u{26A1}",
    title: "MCP Server",
    description: "Claude Code, Cursor, and Windsurf call Memvra tools automatically via the Model Context Protocol."
  },
  {
    icon: "\u{1F4E6}",
    title: "Wrap Any Tool",
    description: "memvra wrap gemini launches any CLI tool with project context pre-loaded and captures the session on exit."
  },
  {
    icon: "\u{1F4E4}",
    title: "Auto-Export",
    description: "CLAUDE.md, .cursorrules, PROJECT_CONTEXT.md, and JSON — regenerated automatically on every change."
  },
  {
    icon: "\u{1F512}",
    title: "Local-First",
    description: "All data stays in .memvra/ on your machine. No accounts, no cloud, no telemetry. MIT licensed."
  }
]
</script>
