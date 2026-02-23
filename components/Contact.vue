<template>
  <section id="contact" class="py-20">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-primary retro-glow">
        {{ '< Contact />' }}
      </h2>

      <div class="max-w-2xl mx-auto">
        <div class="flex flex-wrap gap-8 justify-between">
          <div class="flex items-center space-x-4">
            <div class="w-10 h-10 bg-primary/20 rounded-lg flex items-center justify-center min-w-10 min-h-10">
              <Mail class="w-5 h-5 text-primary min-w-5 min-h-5" />
            </div>
            <div>
              <h3 class="font-semibold mb-1">Email</h3>
              <p class="text-muted-foreground">giulianomaradei@gmail.com</p>
            </div>
          </div>

          <div class="flex items-center space-x-4">
            <div class="w-10 h-10 bg-primary/20 rounded-lg flex items-center justify-center min-w-10 min-h-10">
              <Github class="w-5 h-5 text-primary min-w-5 min-h-5" />
            </div>
            <div>
              <h3 class="font-semibold mb-1">GitHub</h3>
              <p class="text-muted-foreground">github.com/giulianomaradei</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Mail, Phone, Github } from 'lucide-vue-next'
</script>