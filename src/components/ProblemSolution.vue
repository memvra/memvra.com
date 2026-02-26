<template>
  <section class="px-6 py-20 sm:py-28">
    <div class="mx-auto max-w-6xl">
      <h2 class="text-3xl sm:text-4xl font-bold text-center mb-16">
        The problem with <span class="gradient-text">AI memory</span>
      </h2>

      <div class="grid md:grid-cols-2 gap-8">
        <!-- Without Memvra -->
        <div class="rounded-xl border border-red-500/20 bg-red-950/10 p-6 sm:p-8">
          <div class="flex items-center gap-2 mb-6">
            <span class="text-red-400 text-lg">&#x2717;</span>
            <h3 class="text-lg font-semibold text-red-400">Without Memvra</h3>
          </div>
          <div class="font-mono text-sm space-y-3">
            <div class="bg-black/30 rounded-lg p-4">
              <p class="text-text-muted mb-2"># Morning — Claude Code</p>
              <p class="text-white">&gt; Design the auth middleware using JWT with RS256...</p>
              <p class="text-green-400 text-xs mt-1">&#10003; 2 hours of productive work</p>
            </div>
            <div class="bg-black/30 rounded-lg p-4">
              <p class="text-text-muted mb-2"># Afternoon — switch to Gemini</p>
              <p class="text-white">&gt; continue</p>
              <p class="text-red-400 text-xs mt-1">&#x2717; "I don't have any context about what you were working on..."</p>
            </div>
            <div class="bg-black/30 rounded-lg p-4 opacity-60">
              <p class="text-text-muted mb-2"># Re-explain everything...</p>
              <p class="text-white">&gt; We're building an API with Go, using JWT auth with RS256, the middleware is in auth/middleware.go, we decided tokens expire in 1h...</p>
              <p class="text-yellow-400 text-xs mt-1">&#9888; 15 minutes wasted re-explaining</p>
            </div>
          </div>
        </div>

        <!-- With Memvra -->
        <div class="rounded-xl border border-green-500/20 bg-green-950/10 p-6 sm:p-8 glow">
          <div class="flex items-center gap-2 mb-6">
            <span class="text-green-400 text-lg">&#10003;</span>
            <h3 class="text-lg font-semibold text-green-400">With Memvra</h3>
          </div>
          <div class="font-mono text-sm space-y-3">
            <div class="bg-black/30 rounded-lg p-4">
              <p class="text-text-muted mb-2"># Morning — Claude Code (MCP auto-saves)</p>
              <p class="text-white">&gt; Design the auth middleware using JWT with RS256...</p>
              <p class="text-green-400 text-xs mt-1">&#10003; Session saved automatically via MCP</p>
            </div>
            <div class="bg-black/30 rounded-lg p-4">
              <p class="text-text-muted mb-2"># Afternoon — switch to Gemini</p>
              <p class="text-primary text-xs mb-1">$ memvra wrap gemini</p>
              <p class="text-text-muted text-xs">[memvra] injecting project context...</p>
              <p class="text-white">&gt; continue</p>
              <p class="text-green-400 text-xs mt-1">&#10003; "I see you were implementing JWT auth middleware with RS256. Let me continue with the rate limiting..."</p>
            </div>
            <div class="bg-black/30 rounded-lg p-4">
              <p class="text-text-muted mb-2"># Evening — open Cursor</p>
              <p class="text-text-muted text-xs">Cursor reads .cursorrules automatically</p>
              <p class="text-green-400 text-xs mt-1">&#10003; Full context: sessions, decisions, conventions</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
