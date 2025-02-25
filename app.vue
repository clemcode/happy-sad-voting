<script setup lang="ts">
const color = ref("neutral");

const changeColor = (mood: string) => {
  color.value = mood;
};
</script>

<template>
  <div class="background" :class="color">
    <div class="container">
      <button class="happy-button" @click="changeColor('happy')">
        Happy 😎
      </button>
      <button class="sad-button" @click="changeColor('sad')">Sad 😭</button>
    </div>
  </div>
</template>

<style>
body {
  margin: 0;
}

.background {
  height: 100dvh;
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center; /* Center elements horizontally */
}

.container {
  display: flex;
  flex-direction: column; /* Align children (buttons) vertically */
  height: 100%; /* Take full height to align buttons properly */
  justify-content: space-between; /* Distribute space between buttons */
}

button {
  padding: 1rem;
  margin: 1rem 0;
}
.neutral {
  background-color: white;
}

.happy {
  background-color: greenyellow;
}

.sad {
  background-color: red;
}
</style>
