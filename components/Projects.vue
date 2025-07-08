<template>
  <section id="projects" class="py-20 bg-card/30">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-primary retro-glow">
        {{ '< Recent Projects />' }}
      </h2>
      
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div 
          v-for="project in projects"
          :key="project.title"
          class="bg-card border border-border rounded-lg overflow-hidden hover:border-primary/50 transition-all duration-300 group flex flex-col"
        >
          <div class="relative h-64 bg-gradient-to-br from-primary/20 to-accent/20 flex items-center justify-center overflow-hidden">
            <img 
              :src="project.image" 
              :alt="project.title"
              class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-300"
            />
            <div class="absolute top-4 right-4 bg-primary/20 text-primary px-2 py-1 rounded text-xs font-mono backdrop-blur-sm">
              {{ project.category }}
            </div>
          </div>
          
          <div class="p-6 flex flex-1 flex-col justify-between">
            <div>
              <h3 class="text-xl font-bold mb-3 text-foreground group-hover:text-primary transition-colors">
                {{ project.title }}
              </h3>
              
              <p class="text-muted-foreground mb-4 leading-relaxed text-sm">
                {{ project.description }}
              </p>
              
              <div class="mb-4">
                <h4 class="text-sm font-semibold text-foreground mb-2">My Role:</h4>
                <p class="text-muted-foreground text-sm leading-relaxed">
                  {{ project.myRole }}
                </p>
              </div>
            </div>

            <div>
              <div class="flex flex-wrap gap-2 mb-4">
                <span 
                  v-for="tech in project.tech"
                  :key="tech"
                  class="px-2 py-1 bg-primary/10 text-primary rounded text-xs font-mono border border-primary/20"
                >
                  {{ tech }}
                </span>
              </div>
              
              <div class="flex space-x-4">
                <a 
                  :href="project.live"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="flex items-center text-muted-foreground hover:text-primary transition-colors"
                >
                  <ExternalLink :size="16" class="mr-2" />
                  Visit Site
                </a>
              </div>
            </div>
            
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ExternalLink, Code2 } from 'lucide-vue-next'

const projects = [
  {
    title: 'Patio3D',
    description: 'A powerful 3D patio configurator that processes hundreds of engineering logics to calculate the optimal build within milliseconds!',
    myRole: 'Worked on the project from the beginning, converting complex engineering logic to code, working on 3D rendering, creating cache systems for geological data used in engineering, where data analysis and logic were essential, plus working on all core functionalities.',
    tech: ['Nuxt.js', 'Laravel', 'TresJS', 'Multi-tenant', '3D Rendering', 'Engineering Logic'],
    live: 'https://patio3d.com/',
    category: 'Full Stack + 3D',
    image: '/aluma.png'
  },
  {
    title: 'CultureCore',
    description: 'A custom-built employee recognition platform where team members appreciate peers, earn awards and "bucks", and redeem debit and gift cards.',
    myRole: 'Worked on it from the beginning, a complete social network. Worked on third-party service integrations, in-app store, complex comment systems, posts, profiles, and many core system functionalities.',
    tech: ['Nuxt.js', 'Laravel', 'Social Network', 'Payment Integration', 'Real-time'],
    live: 'https://theculturecore.co/',
    category: 'Full Stack',
    image: '/culture.png'
  },
  {
    title: 'ApexReportGen',
    description: 'An AI-powered psychological report generator that helps doctors produce reports based on the DSM-5 in just 10 minutes compared to 5 hours previously!',
    myRole: 'Worked on various core features, plus worked extensively with creating effective prompts, using prompt engineering techniques to optimize AI-generated reports.',
    tech: ['Nuxt.js', 'Laravel', 'Stripe', 'Azure AI', 'Prompt Engineering', 'DSM-5'],
    live: 'https://assess.apexreportgen.com/',
    category: 'AI + Full Stack',
    image: '/apex.png'
  }
]
</script> 