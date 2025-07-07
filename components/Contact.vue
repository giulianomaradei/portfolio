<template>
  <section id="contact" class="py-20">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl md:text-4xl font-bold text-center mb-16 text-primary retro-glow">
        {{ '< Contact />' }}
      </h2>
      
      <div class="max-w-4xl mx-auto">
        <div class="text-center mb-12">
          <p class="text-lg text-muted-foreground">
            Ready to bring your ideas to life? Let's collaborate and build something amazing together.
          </p>
        </div>
        
        <div class="grid md:grid-cols-2 gap-12">
          <div class="space-y-8">
            <div class="flex items-start space-x-4">
              <div class="w-10 h-10 bg-primary/20 rounded-lg flex items-center justify-center">
                <Mail class="w-5 h-5 text-primary" />
              </div>
              <div>
                <h3 class="font-semibold mb-1">Email</h3>
                <p class="text-muted-foreground">giuliano.maradei@example.com</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-4">
              <div class="w-10 h-10 bg-primary/20 rounded-lg flex items-center justify-center">
                <Phone class="w-5 h-5 text-primary" />
              </div>
              <div>
                <h3 class="font-semibold mb-1">Phone</h3>
                <p class="text-muted-foreground">+1 (555) 123-4567</p>
              </div>
            </div>
            
            <div class="flex items-start space-x-4">
              <div class="w-10 h-10 bg-primary/20 rounded-lg flex items-center justify-center">
                <MapPin class="w-5 h-5 text-primary" />
              </div>
              <div>
                <h3 class="font-semibold mb-1">Location</h3>
                <p class="text-muted-foreground">Available for remote work</p>
              </div>
            </div>
          </div>
          
          <div class="bg-card border border-border rounded-lg p-6">
            <form @submit.prevent="submitForm" class="space-y-4">
              <div>
                <label class="block text-sm font-medium mb-2 text-foreground">Name</label>
                <input 
                  v-model="form.name"
                  type="text" 
                  class="w-full px-4 py-2 bg-background border border-border rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent outline-none transition-all"
                  placeholder="Your name"
                  required
                />
              </div>
              
              <div>
                <label class="block text-sm font-medium mb-2 text-foreground">Email</label>
                <input 
                  v-model="form.email"
                  type="email" 
                  class="w-full px-4 py-2 bg-background border border-border rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent outline-none transition-all"
                  placeholder="your.email@example.com"
                  required
                />
              </div>
              
              <div>
                <label class="block text-sm font-medium mb-2 text-foreground">Message</label>
                <textarea 
                  v-model="form.message"
                  rows="4"
                  class="w-full px-4 py-2 bg-background border border-border rounded-lg focus:ring-2 focus:ring-primary focus:border-transparent outline-none transition-all resize-none"
                  placeholder="Tell me about your project..."
                  required
                ></textarea>
              </div>
              
              <button 
                type="submit"
                class="w-full px-6 py-3 bg-primary text-primary-foreground rounded-lg font-semibold hover:bg-primary/90 transition-all hover:scale-105"
              >
                Send Message
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Mail, MapPin, Phone } from 'lucide-vue-next'
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  message: ''
})

const submitForm = () => {
  // Handle form submission
  console.log('Form submitted:', form.value)
  // Reset form
  form.value = {
    name: '',
    email: '',
    message: ''
  }
}
</script> 