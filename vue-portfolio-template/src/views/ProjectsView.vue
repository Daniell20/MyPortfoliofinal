<script setup>
import MainLayout from '../components/MainLayout.vue';

// Page Title of Views
const pageTitle = 'Projects'
</script>

<template>
  <MainLayout :pageTitle="pageTitle">
    <section>
      My Current Project 
    </section>
    <div class="mb-8"></div>

    <router-link to="/projects" href="#" class="group relative flex h-48 items-end overflow-hidden rounded-lg bg-gray-100 shadow-lg md:h-80">
      <img src="../assets/debt.png"
          loading="lazy" alt="debtstore"
          class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110" />

      <div
          class="pointer-events-none absolute inset-0 bg-gradient-to-t from-gray-800 via-transparent to-transparent opacity-50">
      </div>

      <span class="relative ml-4 mb-3 inline-block text-sm text-white md:ml-5 md:text-lg">DEBT STORE APP</span>
  </router-link>
  <div class="mb-2"></div>

    <router-link to="/projects"
                class="group relative flex h-48 items-end overflow-hidden rounded-lg bg-gray-100 shadow-lg md:col-span-2 md:h-80">
                <img src="../assets/vuepic.png"
                    loading="lazy" alt="vue"
                    class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110" />

                <div
                    class="pointer-events-none absolute inset-0 bg-gradient-to-t from-gray-800 via-transparent to-transparent opacity-50">
                </div>

                <span class="relative ml-4 mb-3 inline-block text-sm text-white md:ml-5 md:text-lg">VUE</span>
                
            </router-link>
            <div class="mb-2"></div>

            <router-link to="/projects"
                class="group relative flex h-48 items-end overflow-hidden rounded-lg bg-gray-100 shadow-lg md:col-span-2 md:h-80">
                <img src="../assets/chatapp.png"
                    loading="lazy" alt="chatapp"
                    class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110" />

                <div
                    class="pointer-events-none absolute inset-0 bg-gradient-to-t from-gray-800 via-transparent to-transparent opacity-50">
                </div>

                <span class="relative ml-4 mb-3 inline-block text-sm text-white md:ml-5 md:text-lg">CHAT APP</span>
            </router-link>
            <div class="mb-2"></div>

            <router-link to="/vuegames/introvuegames" class="group relative flex h-48 items-end overflow-hidden rounded-lg bg-gray-100 shadow-lg md:h-80">
              <img src="../assets/vuegames.png"
                  loading="lazy" alt="vuegames"
                  class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110" />

              <div
                  class="pointer-events-none absolute inset-0 bg-gradient-to-t from-gray-800 via-transparent to-transparent opacity-50">
              </div>

              <span class="relative ml-4 mb-3 inline-block text-sm text-white md:ml-5 md:text-lg">VUE GAMES</span>
          </router-link>
          
  </MainLayout>
</template>