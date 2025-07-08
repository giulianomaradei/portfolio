<template>
  <section id="about" class="py-20 bg-card/30">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-primary retro-glow">
        {{ '< About />' }}
      </h2>
      
      <div class="max-w-4xl mx-auto">
        <div class="grid md:grid-cols-2 gap-12">
          <div class="space-y-6">
            <p class="text-muted-foreground leading-relaxed">
              I build scalable web applications that solve real problems. From 3D configurators to social platforms, I've delivered solutions across multiple industries using Laravel and Nuxt.js.
            </p>
            
            <p class="text-muted-foreground leading-relaxed">
              My competitive programming background drives me to find elegant solutions to complex challenges. I handle the full development cycle — from architecture to deployment.
            </p>

            <p class="text-muted-foreground leading-relaxed">
              And i also can bench 120kg, what more a company would need? 🤔 
            </p>
            
            <div class="flex flex-wrap gap-2 mt-6">
              <span 
                v-for="trait in traits"
                :key="trait"
                class="px-3 py-1 bg-primary/20 text-primary rounded-full text-sm border border-primary/30"
              >
                {{ trait }}
              </span>
            </div>
          </div>
          
          <div class="bg-card border border-border rounded-lg p-6 font-mono text-sm h-fit">
            <div class="text-primary mb-2">const giuliano = {{ '{' }}</div>
            <div class="pl-4 space-y-1">
              <div><span class="text-accent">name:</span> <span class="text-yellow-400">"Giuliano Maradei"</span>,</div>
              <div><span class="text-accent">role:</span> <span class="text-yellow-400">"Software Developer"</span>,</div>
              <div><span class="text-accent">location:</span> <span class="text-yellow-400">"Earth"</span>,</div>
              <div><span class="text-accent">passion:</span> <span class="text-yellow-400">"Building awesome stuff"</span>,</div>
            </div>
            <div class="text-primary">{{ '}' }}</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const traits = ['Problem Solver', 'Self-taught', 'Challenge-driven', 'Social', 'Strong']
</script> 