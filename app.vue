<template>
  <div class="min-h-screen bg-background text-foreground">
    <Header />
    <Hero />
    <About />
    <Skills />
    <Projects />
    <Contact />
    <Footer />
  </div>
</template>

<script setup lang="ts">
import Header from '~/components/Header.vue'
import Hero from '~/components/Hero.vue'
import About from '~/components/About.vue'
import Skills from '~/components/Skills.vue'
import Projects from '~/components/Projects.vue'
import Contact from '~/components/Contact.vue'
import Footer from '~/components/Footer.vue'
</script>
