<template>
  <div class="jokes-container">
    <div class="jokes-generator">
      <h2 class="text-4xl font-bold uppercase mb-4">Jokes Generator</h2>
    </div>
    <div class="type-box mt-4 p-4 bg-white border border-gray-300 rounded text-center text-lg text-gray-700">
      {{ joke }}
      
    </div>
    <button
        @click="generateJoke"
        :disabled="loading"
        class="mt-4 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded relative"
      >
        Generate Joke
        <div v-if="loading" class="loading-indicator"></div>
      </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jokes: [
        "ngano man sge duko ang biik? Answer: kay mauwaw sila kay ila mama baboy",
        "Ano sabi ng kilay sa katabi nyang kilay? Answer:hi brow",
        "Meron akong jokes tungkol sa unggoy.di ko pwede sabhn kasi baka magalit ka",
        "ano ang cellphone ang pinakamatanda? Answer:Motolola",
        
        // Add more jokes to the array
      ],
      joke: "Please click Gently!!! ",
      loading: false,
    };
  },
  methods: {
    generateJoke() {
      this.loading = true;
      // Simulate an asynchronous operation (e.g., fetching a joke from an API)
      setTimeout(() => {
        const randomIndex = Math.floor(Math.random() * this.jokes.length);
        this.joke = this.jokes[randomIndex];
        this.loading = false;
      }, 1500); // Simulating a delay of 1.5 seconds
    },
  },
};
</script>

<style scoped>
.jokes-container {
  @apply flex flex-col items-center justify-center h-screen bg-gray-100 p-8 rounded shadow-md mt-8;
}

.jokes-generator {
  @apply mb-4;
}

.type-box {
  @apply mt-4 p-4 bg-white border border-gray-300 rounded text-center text-lg text-gray-700;
}

.loading-indicator {
  @apply absolute top-0 right-0 bottom-0 left-0 m-auto; /* Center the loading indicator */
  border: 4px solid rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  border-top: 4px solid #fff;
  width: 20px;
  height: 20px;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
</style>
