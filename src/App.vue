<script setup>
import { ref } from 'vue'

const money = ref(0)

function addMoney() {
  money.value++
}

</script>

<template>
  <video autoplay loop muted class="video">
    <source src="./assets/hide_da_money_yall.mp4" type="video/mp4">
  </video>
  <header>
    <div class="wrapper">
      <h1>Click down below to hide money !</h1>
      <button @click="addMoney">Money hidden : {{ money }} $</button>
    </div>
  </header>
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

@media (min-width: 1024px) {

  .video {
    z-index: -1000; 
    left: 50%;
    width: 100vw;
    height: 100vh;
    position: absolute;
    top: 50%;
    --webkit-transform: translate(-50% , -50%);
    --moz-transform: translate(-50% , -50%);
    transform: translate(-50% , -50%);
    object-fit: cover;
  }

  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    display: flex;
    justify-content: center;
    flex-direction: column;
  }

  .wrapper h1 {
    color: white;
  }

  .wrapper button {
    margin-top: 30px;
    width: fit-content;
    padding: 20px;
    color: none;
    border: 2px solid white;
  }

}
</style>
