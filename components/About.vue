<template>
  <section id="about" class="py-20 bg-card/30">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-primary retro-glow">
        {{ '< About />' }}
      </h2>
      
      <div class="max-w-4xl mx-auto">
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <div class="space-y-6">
            <p class="text-muted-foreground leading-relaxed">
              I'm a passionate software developer with a love for creating innovative 
              solutions that make a difference. My journey in tech has been driven by 
              curiosity and a constant desire to learn and grow.
            </p>
            
            <p class="text-muted-foreground leading-relaxed">
              With experience across various technologies and frameworks, I specialize 
              in building scalable web applications and solving complex technical challenges. 
              I believe in writing clean, maintainable code that stands the test of time.
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
          
          <div class="bg-card border border-border rounded-lg p-6 font-mono text-sm">
            <div class="text-primary mb-2">const giuliano = {{ '{' }}</div>
            <div class="pl-4 space-y-1">
              <div><span class="text-accent">name:</span> <span class="text-yellow-400">"Giuliano Maradei"</span>,</div>
              <div><span class="text-accent">role:</span> <span class="text-yellow-400">"Software Developer"</span>,</div>
              <div><span class="text-accent">location:</span> <span class="text-yellow-400">"Earth"</span>,</div>
              <div><span class="text-accent">experience:</span> <span class="text-yellow-400">"5+ years"</span>,</div>
              <div><span class="text-accent">passion:</span> <span class="text-yellow-400">"Building awesome stuff"</span>,</div>
              <div><span class="text-accent">coffee:</span> <span class="text-yellow-400">true</span></div>
            </div>
            <div class="text-primary">{{ '}' }}</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const traits = ['Problem Solver', 'Team Player', 'Continuous Learner', 'Innovation Driven']
</script> 