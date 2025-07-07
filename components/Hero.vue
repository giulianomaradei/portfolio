<template>
  <section class="min-h-screen flex items-center justify-center pt-20 relative">
    <div class="container mx-auto px-6 text-center">
      <div class="animate-fade-in">
        <h1 class="text-5xl md:text-7xl font-bold mb-6">
          <span class="text-muted-foreground">Hello, I'm</span>
          <br />
          <span class="gradient-text">Giuliano Maradei</span>
        </h1>
        
        <div class="text-xl md:text-2xl text-muted-foreground mb-8 font-mono">
          <span class="text-primary">{{ '> ' }}</span>
          Software Developer
          <span class="animate-pulse text-primary">_</span>
        </div>
        
        <p class="text-lg text-muted-foreground max-w-2xl mx-auto mb-12 leading-relaxed">
          I craft digital experiences through code, building robust applications 
          and solving complex problems with elegant solutions. Welcome to my digital space.
        </p>
        
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <button 
            @click="scrollToProjects"
            class="px-8 py-3 bg-primary text-primary-foreground rounded-lg font-semibold hover:bg-primary/90 transition-all hover:scale-105"
          >
            View My Work
          </button>
          <button 
            @click="scrollToContact"
            class="px-8 py-3 border border-primary text-primary rounded-lg font-semibold hover:bg-primary/10 transition-all hover:scale-105"
          >
            Get In Touch
          </button>
        </div>
      </div>
      
      <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
        <div class="w-6 h-10 border-2 border-primary rounded-full flex justify-center">
          <div class="w-1 h-3 bg-primary rounded-full mt-2 animate-pulse"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const scrollToProjects = () => {
  const element = document.getElementById('projects')
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}

const scrollToContact = () => {
  const element = document.getElementById('contact')
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}
</script> 