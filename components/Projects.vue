<template>
  <section id="projects" class="py-20 bg-card/30">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-primary retro-glow">
        {{ '< Experience />' }}
      </h2>

      <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
        <div
          v-for="exp in experiences"
          :key="exp.company"
          class="bg-card border border-border rounded-lg p-6 hover:border-primary/50 transition-all duration-300 flex flex-col"
        >
          <div class="flex flex-wrap items-center gap-2 mb-3">
            <span class="text-xs font-mono text-primary bg-primary/10 px-2 py-1 rounded border border-primary/20">
              {{ exp.period }}
            </span>
            <span v-if="exp.duration" class="text-xs text-muted-foreground">
              {{ exp.duration }}
            </span>
          </div>
          <h3 class="text-xl font-bold mb-1 text-foreground">
            {{ exp.role }} — {{ exp.company }}
          </h3>
          <p v-if="exp.companyUrl" class="text-sm text-muted-foreground" :class="exp.location ? 'mb-1' : 'mb-3'">
            {{ exp.companyUrl }}
          </p>
          <p v-if="exp.location" class="text-sm text-muted-foreground mb-3">
            {{ exp.location }}
          </p>
          <p class="text-muted-foreground leading-relaxed text-sm mb-4 flex-1">
            {{ exp.description }}
          </p>
          <div class="flex flex-wrap gap-2">
            <span
              v-for="tech in exp.tech"
              :key="tech"
              class="px-2 py-1 bg-primary/10 text-primary rounded text-xs font-mono border border-primary/20"
            >
              {{ tech }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const experiences = [
  {
    role: 'Full-stack Developer',
    company: 'RedLayers',
    location: 'London, United Kingdom · Remote',
    period: 'Jan 2024 – Aug 2025',
    duration: '1 yr 8 mos',
    description: 'Full-stack developer across the full cycle: planning, development, UI/UX, testing, deployment. Nuxt for SSR SPAs, Laravel for APIs; integrations with Azure OpenAI (prompt engineering), Stripe, and Cloudflare. Contributed to a 3D configurator, employee recognition platform, and AI report generation.',
    tech: ['Nuxt.js', 'Vue.js', 'Laravel', 'TypeScript', 'Stripe', 'Azure OpenAI']
  },
  {
    role: 'Full Stack Developer',
    company: 'Sync360',
    period: 'Apr 2023 – Dec 2023',
    location: 'Bragança Paulista, Brazil · Remote',
    duration: '9 mos',
    description: 'During my role as a full-stack developer at Sync360.io, I was part of a team that developed customized web solutions for clients from various industries. My responsibilities included project planning, front-end interface development, back-end API development, refactoring of legacy code, and maintenance of various systems.',
    tech: ['PHP', 'Server-side', 'Front-end', 'Back-end', 'API', 'Refactoring']
  },
  {
    role: 'Back End Developer',
    company: 'Pigmo',
    period: 'Jul 2022 – Feb 2023',
    location: 'Remote',
    duration: '8 mos',
    description: 'As a Backend Developer using Laravel at crashout.io, I was pivotal in maintaining and creating features for the website\'s core functionality. My responsibilities encompassed creating robust CRUD operations, formulating essential business rules, and bug-solving.',
    tech: ['PHP', 'Laravel', 'Back-end', 'CRUD']
  }
]
</script>
