<script setup>
import Tilt from 'vanilla-tilt-vue'
import me from 'assets/images/me.svg'
const aboutInit = '<p>'
const aboutEnd = '</p>'

const colorMode = useColorMode()
console.log(colorMode.preference)
</script>

<template>
  <nav class="bg-indigo-800 font-mono">
    <div class="max-w-5xl mx-auto">
      <div class="flex items-center justify-between px-4 py-6">
        <div>
          <p class="text-gray-100 font-bold">Mateus Reis <span class="text-teal-400 font-bold">/></span></p>
        </div>
        <div class="text-gray-900 dark:text-gray-100 space-x-6">
          <a href="">Home</a>
          <a href="">About</a>
          <a href="">Work</a>
          <a href="">Contacts</a>
          <a class="bg-teal-400 text-indigo-800 font-bold p-3" href="">Brief me /> </a>
          <h1>Color mode: {{ $colorMode.value }}</h1>
          <select v-model="$colorMode.preference">
            <option value="system">System</option>
            <option value="light">Light</option>
            <option value="dark">Dark</option>
            <option value="sepia">Sepia</option>
          </select>
        </div>
      </div>
    </div>
  </nav>
  <section id="home" class="bg-gray-200 dark:bg-gray-800 font-mono">
    <div class="max-w-5xl mx-auto">
      <div class="grid grid-cols-2 gap-8 px-4 py-20">
        <div class="space-y-6">
          <h2
            class="text-6xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-teal-700 dark:from-teal-300 to-indigo-700 dark:to-indigo-300">
            Bring your brand to life with your help</h2>
          <p class="text-gray-900 dark:text-gray-100 font-sans">In your role as a professional web developer, you're up
            for just about any
            website-building challenge.
          </p>
          <a type="button"
            class="bg-teal-900 border border-teal-400 hover:bg-teal-800 text-gray-100 font-bold px-6 py-4"
            href="">Contact />
          </a>
          <div class="text-gray-500 grid grid-cols-4 gap-2">
            <a type="button" href="" class="flex items-center space-x-2 hover:text-teal-400">
              <iconGitHub />
              <span>Github</span>
            </a>
            <a type="button" href="" class="flex items-center space-x-2 hover:text-teal-400">
              <IconLinkedIn />
              <span>LinkedIn</span>
            </a>
          </div>
        </div>
        <div class="flex items-center justify-center">
          <Tilt>
            <img class="w-96 h-96 rounded-full bg-teal-200" :src="me" alt="me">
          </Tilt>
        </div>
      </div>

    </div>
  </section>
  <div class="w-full h-[1px] bg-teal-400"></div>
  <section id="about" class="bg-gray-200 dark:bg-gray-800 font-mono">
    <div class="max-w-5xl mx-auto">
      <div class="grid grid-cols-2 gap-20 px-4 py-20">
        <div>
          <h3 class="text-gray-800 dark:text-gray-100 text-3xl">About me</h3>
          <div class="text-teal-600 dark:text-teal-400 pt-8">
            <p>{{ aboutInit }} <br>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis voluptas expedita repellat nulla quis
              vero quibusdam nisi impedit ipsam eveniet? Voluptas sunt alias totam atque quasi magni officia rerum
              saepe!
              <br>
              {{ aboutEnd }}
            </p>
          </div>
        </div>
        <div>
          <div class="w-full h-1 bg-teal-400 mt-4 mb-12 "></div>
          <div class="space-y-8">
            <p class="text-gray-800 dark:text-gray-100 font-sans">
              A front-end developer's role is to combine design and business logic to achieve a user-facing product. A
              wide skill set is necessary to produce a quality user experience that leads to meeting business goals.
            </p>
            <ul class="text-gray-800 dark:text-gray-100 font-sans list-disc list-inside">
              <li>Create responsive websites that work on a wide range of devices</li>
              <li>Assist with production of clean and functional design</li>
              <li>Bridge communication gap between designers and developers</li>
              <li>Integrate your website into an easy to use content management system </li>
            </ul>
            <p class="text-gray-800 dark:text-gray-100 font-sans">The work I provide is of highest quality, fully
              responsive, and
              tested in a wide range of devices.</p>
            <a type="button"
              class="bg-teal-900 border border-teal-400 hover:bg-teal-800 text-gray-100 font-bold px-4 py-3"
              href="">LinkedIn profile />
            </a>
          </div>

        </div>
      </div>

    </div>
  </section>
  <div class="w-full h-[1px] bg-teal-400"></div>

  <section id="work" class="bg-gray-200 dark:bg-gray-800 font-mono">
    <div class="max-w-5xl mx-auto">
      <div class="grid grid-cols-2 gap-20 px-4 pt-20">
        <div>
          <h3 class="text-gray-800 dark:text-gray-100 text-3xl">Recent work</h3>
        </div>
        <div>
          <div class="w-full h-1 bg-teal-400 mt-4 mb-12 "></div>
        </div>
      </div>
      <div class="grid grid-cols-3 gap-10 px-4 pb-20">
        <nuxt-img src="https://matriculas.estacio.br/blog/wp-content/uploads/2020/01/30estacio08-eng-software.jpg"
          quality="80" width="512" height="512" />
        <nuxt-img src="https://matriculas.estacio.br/blog/wp-content/uploads/2020/01/30estacio08-eng-software.jpg"
          quality="80" width="512" height="512" />
        <nuxt-img src="https://matriculas.estacio.br/blog/wp-content/uploads/2020/01/30estacio08-eng-software.jpg"
          quality="80" width="512" height="512" />
      </div>
    </div>
  </section>
</template>
