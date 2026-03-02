<template>
  <section class="px-6 py-20 sm:py-28">
    <div class="mx-auto max-w-5xl">
      <h2 class="text-3xl sm:text-4xl font-bold text-center mb-4">
        Not just <span class="gradient-text">session migration</span>
      </h2>
      <p class="text-text-muted text-center text-lg mb-16 max-w-2xl mx-auto">
        Memvra builds long-term project memory, not just a bridge between tools
      </p>

      <div class="grid md:grid-cols-2 gap-8">
        <!-- Session Migration Tools -->
        <div class="rounded-xl border border-border bg-surface-light p-6 sm:p-8">
          <h3 class="text-xl font-semibold mb-4 text-text-muted">Session Migration Tools</h3>
          <ul class="space-y-3 text-sm text-text-muted">
            <li class="flex items-start gap-3">
              <span class="text-yellow-400 mt-0.5">→</span>
              <span>Resume your most recent conversation when switching AI tools</span>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-yellow-400 mt-0.5">→</span>
              <span>One-time use when you hit rate limits</span>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-yellow-400 mt-0.5">→</span>
              <span>Read existing session files from AI tools</span>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-yellow-400 mt-0.5">→</span>
              <span>Reactive: only useful when switching tools</span>
            </li>
          </ul>
          <p class="mt-6 text-xs text-text-muted italic border-t border-border pt-4">
            Good for: Quick handoffs when you hit API limits
          </p>
        </div>

        <!-- Memvra -->
        <div class="rounded-xl border border-primary/30 bg-gradient-to-br from-primary/5 to-accent/5 p-6 sm:p-8 glow">
          <h3 class="text-xl font-semibold mb-4 text-primary">Memvra</h3>
          <ul class="space-y-3 text-sm">
            <li class="flex items-start gap-3">
              <span class="text-green-400 mt-0.5">✓</span>
              <span>Builds persistent knowledge base over time</span>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-green-400 mt-0.5">✓</span>
              <span>Always-on infrastructure with vector search & decision tracking</span>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-green-400 mt-0.5">✓</span>
              <span>Auto-indexes your codebase and remembers "why" decisions were made</span>
            </li>
            <li class="flex items-start gap-3">
              <span class="text-green-400 mt-0.5">✓</span>
              <span>Proactive: every session benefits from accumulated knowledge</span>
            </li>
          </ul>
          <p class="mt-6 text-xs italic border-t border-primary/20 pt-4">
            Good for: Long-term project memory that improves every AI session
          </p>
        </div>
      </div>

      <!-- Key Difference Callout -->
      <div class="mt-12 rounded-xl bg-primary/10 border border-primary/20 p-6 text-center">
        <p class="text-lg">
          <span class="font-semibold text-primary">Key difference:</span>
          <span class="text-text-muted"> Memvra isn't just about switching tools — it's about never having to re-explain your project in the first place.</span>
        </p>
      </div>
    </div>
  </section>
</template>
