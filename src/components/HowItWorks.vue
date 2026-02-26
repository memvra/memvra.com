<template>
  <section class="px-6 py-20 sm:py-28">
    <div class="mx-auto max-w-5xl">
      <h2 class="text-3xl sm:text-4xl font-bold text-center mb-4">
        How it <span class="gradient-text">works</span>
      </h2>
      <p class="text-text-muted text-center text-lg mb-16 max-w-2xl mx-auto">
        Three steps. Every AI tool gets your project context.
      </p>

      <div class="grid md:grid-cols-3 gap-8">
        <div v-for="(step, i) in steps" :key="i" class="text-center">
          <div class="inline-flex items-center justify-center w-12 h-12 rounded-full bg-primary/10 border border-primary/30 text-primary font-bold text-lg mb-6">
            {{ i + 1 }}
          </div>
          <h3 class="text-lg font-semibold mb-3">{{ step.title }}</h3>
          <div class="bg-surface-light border border-border rounded-lg p-4 font-mono text-sm text-left mb-4">
            <span class="text-text-muted">$ </span><span class="text-white">{{ step.command }}</span>
          </div>
          <p class="text-text-muted text-sm leading-relaxed">{{ step.description }}</p>
        </div>
      </div>

      <!-- Architecture diagram -->
      <div class="mt-20 rounded-xl border border-border bg-surface-light p-6 sm:p-8">
        <h3 class="text-lg font-semibold text-center mb-6">Under the hood</h3>
        <div class="font-mono text-xs sm:text-sm text-text-muted leading-relaxed overflow-x-auto">
          <pre class="text-center">
Source files ──► Scanner ──► Chunker ──► Embedder
                                           │
                    ┌──────────────────────────────────┐
                    │    .memvra/memvra.db (SQLite)     │
                    │    memories · sessions · vectors  │
                    └──────────────────────────────────┘
                                    │
                  ┌─────────────────┼─────────────────┐
                  ▼                 ▼                  ▼
            LLM Provider      Auto-Export         MCP Server
          (Claude/Gemini/    CLAUDE.md            Claude Code
           OpenAI/Ollama)    .cursorrules          Cursor
                             PROJECT_CONTEXT.md    Windsurf</pre>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  {
    title: "Initialize",
    command: "memvra init",
    description: "Scans your project, detects tech stack, chunks source files, and creates vector embeddings."
  },
  {
    title: "Work with any AI",
    command: "memvra wrap gemini",
    description: "Use MCP tools, wrap CLI tools, or ask directly. Sessions and decisions are saved automatically."
  },
  {
    title: "Switch seamlessly",
    command: "# open Cursor, type 'continue'",
    description: "Context follows you everywhere. CLAUDE.md, .cursorrules, and JSON are always up to date."
  }
]
</script>
