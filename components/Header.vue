<template>
  <header class="fixed top-0 left-0 right-0 z-50 bg-background/80 backdrop-blur-sm border-b border-border">
    <div class="container mx-auto px-6 py-4 flex justify-between items-center">
      <div class="text-xl font-bold text-primary retro-glow">
        {{ '<GM />' }}
      </div>
      
      <nav class="hidden md:flex space-x-8">
        <a href="#about" class="text-muted-foreground hover:text-primary transition-colors">
          About
        </a>
        <a href="#skills" class="text-muted-foreground hover:text-primary transition-colors">
          Skills
        </a>
        <a href="#projects" class="text-muted-foreground hover:text-primary transition-colors">
          Projects
        </a>
        <a href="#contact" class="text-muted-foreground hover:text-primary transition-colors">
          Contact
        </a>
      </nav>

      <div class="flex space-x-4">
        <a 
          href="https://github.com" 
          class="text-muted-foreground hover:text-primary transition-colors"
          target="_blank"
          rel="noopener noreferrer"
        >
          <Github :size="20" />
        </a>
        <a 
          href="https://linkedin.com" 
          class="text-muted-foreground hover:text-primary transition-colors"
          target="_blank"
          rel="noopener noreferrer"
        >
          <Linkedin :size="20" />
        </a>
        <a 
          href="mailto:giuliano@example.com" 
          class="text-muted-foreground hover:text-primary transition-colors"
        >
          <Mail :size="20" />
        </a>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
import { Github, Mail, Linkedin } from 'lucide-vue-next'
</script> 