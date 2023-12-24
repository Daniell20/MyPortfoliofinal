<script setup>
  import MainLayout from '../components/MainLayout.vue';
  
  // Page Title of Views
  const pageTitle = 'About';
  </script>
  
  <template>
    <MainLayout :pageTitle="pageTitle">
      <section class="bg-gray-900 text-white py-8">
        <div class="container mx-auto text-center">
          <p class="text-lg mb-4">
            Let's get to know the author a bit more.
          </p>
        </div>
      </section>
  
      <div class="max-w-full w-full bg-white p-8 rounded-lg shadow-md mx-auto mt-8 text-center">
        <!-- Author Image -->
        <div class="inline-block">
          <img class="rounded-full h-80 w-80" src="../assets/mypic.jpg" alt="Author's Image">
        </div>
  
        <!-- Author Details -->
        <div class="inline-block ml-11 mb-1 text-left">
          <h2 class="text-3xl font-bold text-cyan-800 mb-20">About Me</h2>
  
          <div class="mb-4">
            <h3 class="text-lg font-semibold text-gray-800">
              I'm Rey Earl Galos, a BSIT student at Cordova National High School.
              <br>
              I live in Bangbang, Cordova, Cebu. My hobbies include playing online games
              <br>
              and watching movies and anime.
            </h3>
          </div>
  
          <!-- Form Section (Skills) -->
          <div class="mb-2">
            <span class="mr-2 text-gray-700 font-semibold mb-2">Skills:</span>
            <span class="text-gray-800">Graphics Designer, Animator, Vue.js, HTML, CSS</span>
          </div>
          <div class="flex h-16 items-center justify-center rounded-lg bg-gray-100 p-4 text-gray-400 sm:h-50">
            <svg class="h-6 w-auto sm:h-8" width="186" height="39" viewBox="0 0 186 39" fill="currentColor"
                xmlns="">
                
            </svg>
        </div>
        <br>
          
        </div>
      </div>
    </MainLayout>
  </template>
  