<template>
  <section id="skills" class="py-20">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-primary retro-glow">
        {{ '< Skills />' }}
      </h2>
      
      <div class="grid md:grid-cols-3 lg:grid-cols-3 gap-8">
        <div 
          v-for="category in skillCategories"
          :key="category.title"
          class="bg-card border border-border rounded-lg p-6 hover:border-primary/50 transition-all duration-300 group"
        >
          <div class="flex items-center mb-4">
            <component 
              :is="category.icon" 
              :class="`w-6 h-6 ${category.color} mr-3 group-hover:animate-pulse`" 
            />
            <h3 class="text-xl font-semibold text-foreground">{{ category.title }}</h3>
          </div>
          
          <div class="space-y-2">
            <div 
              v-for="skill in category.skills"
              :key="skill"
              class="text-muted-foreground hover:text-primary transition-colors cursor-default font-mono text-sm"
            >
              {{ '> ' }}{{ skill }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Code, Database, Globe, Zap } from 'lucide-vue-next'

const skillCategories = [
  {
    icon: Code,
    title: 'Frontend',
    skills: ['Vue.js', 'Nuxt.js', 'Tailwind CSS', 'TypeScript', 'Three.js'],
    color: 'text-retro-blue'
  },
  {
    icon: Database,
    title: 'Backend',
    skills: ['Laravel', 'PHP', 'MySQL', "Pest"],
    color: 'text-retro-slate'
  },
  {
    icon: Globe,
    title: 'DevOps',
    skills: ['Docker', 'CI/CD', 'Linux'],
    color: 'text-retro-steel'
  }
]
</script> 