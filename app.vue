<script setup>
import Tilt from 'vanilla-tilt-vue'
import me from 'assets/images/me.svg'

</script>

<template>
  <nav class="bg-indigo-800 font-mono">
    <div class="max-w-5xl mx-auto">
      <div class="flex items-center justify-between px-4 py-6">
        <div>
          <p class="text-gray-100 font-bold">Mateus Reis <span class="text-lime-400 font-bold">/></span></p>
        </div>
        <div class="text-gray-100 space-x-6">
          <a href="">Home</a>
          <a href="">About</a>
          <a href="">Work</a>
          <a href="">Contacts</a>
          <a class="bg-lime-400 text-indigo-800 font-bold p-3" href="">Brief me /> </a>
        </div>
      </div>
    </div>
  </nav>
  <section id="home" class="bg-gray-800 font-mono">
    <div class="max-w-5xl mx-auto">
      <div class="grid grid-cols-2 gap-8 px-4 py-20">
        <div class="space-y-6">
          <h2 class="text-6xl text-white">Bring your brand to life with your help</h2>
          <p class="text-gray-100 font-sans">In your role as a professional web developer, you're up for just about any
            website-building challenge.
          </p>
          <a type="button"
            class="bg-lime-900 border border-lime-400 hover:bg-lime-800 text-gray-100 font-bold px-6 py-4"
            href="">Contact />
          </a>
          <div class="text-gray-500 grid grid-cols-2 gap-2">
            <a type="button" href="" class="flex items-center space-x-2">
              <iconGitHub />
              <span>Github</span>
            </a>
            <a type="button" href="" class="flex items-center space-x-2">
              <IconLinkedIn />
              <span>LinkedIn</span>
            </a>
          </div>
        </div>
        <div class="flex items-center justify-center">
          <Tilt>
            <img class="w-96 h-96 rounded-full bg-lime-200" :src="me" alt="me">
          </Tilt>
        </div>
      </div>

    </div>
  </section>
</template>

