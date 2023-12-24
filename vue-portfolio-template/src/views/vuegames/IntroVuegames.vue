<template>
    <div>
      <div class="gameintro">
        <div class="black-overlay"></div>
        <audio autoplay loop>
          <!-- <source src="../assets/creepy-audio.mp3" type="audio/mpeg"> -->
        </audio>
        <img src="../../assets/funny.jpg" alt="">
        <div class="centered-text">Joke Generator</div>
        <button @click="startGame" class="funny-button">Continue</button>
      </div>
    </div>
  </template>
  <script>
    export default {
      methods: {
        startGame() {
          // Use Vue Router to navigate to the desired route
          this.$router.push('../games'); // Replace '/intro' with your desired route
        },
      },
    };
    </script>
  
  <style>
  .gameintro {
    position: relative;
    height: 100vh;
  }
  
  .black-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: black;
    animation: fadeIn 3s ease-in;
    z-index: 2; /* Place the black overlay above the background image */
    opacity: 0; /* Initially transparent */
  }
  
  @keyframes fadeIn {
    from {
      opacity: 1;
    }
    to {
      opacity: 0;
    }
  }
  
  .gameintro img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    z-index: 1; /* Place the image below the black overlay */
  }
  
  .centered-text {
    background: rgba(255, 255, 255, 0.5); /* Adjust the alpha value (0.0 to 1.0) for transparency */
    background: rgba(255, 255, 255, 0.863);
    position: absolute;
    border-radius: 10px;
    padding: 20px;
    border: 1px solid rgb(254, 254, 254);
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 100px;
    font-family: 'Roboto', sans-serif;
    color: yellow;
    text-shadow: 5px 5px 10px #000;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
    z-index: 3; /* Place the text above the black overlay */
    
  }
  
  .funny-button {
    position: fixed;
    bottom: 10px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 4;
    background-color: green;
    color: #fff;
    border: none;
    border-radius: 10px;
    padding: 15px 30px;
    cursor: pointer;
    font-size: 24px;
    text-transform: uppercase;
    font-weight: bold;
    letter-spacing: 2px;
    text-shadow: 2px 2px 5px #000;
    box-shadow: 0 0 20px #000;
    transition: background-color 0.3s, transform 0.3s;
    margin-bottom: 100px;
    font-family: 'Chewy', cursive; /* Use the Chewy font or another funny font */
    animation: bounce 1s infinite alternate;
    margin-left:-100px;
}

@keyframes bounce {
    0% {
        transform: translateY(0);
    }
    100% {
        transform: translateY(-10px);
    }
}



  
  .funny:hover {
    background-color: #4d0c0c;
    transform: translateX(-50%) scale(1.1);
  }
  </style>
  