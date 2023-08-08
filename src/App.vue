<script setup>
import { ref } from 'vue'
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'
let message = ref('hello world')
let number = ref(10)
function getRandomNumber()
{
  return Math.random()
}
</script>


<template>
  <h1>Text interpolation and data binding</h1>
  <p>{{ message.split(" ").reverse().join(" ") }}</p>
  <p>{{ number + 20 }}</p>
  <p>{{ true ? 'Yes' : 'No' }}</p>
  <p>{{ getRandomNumber() }}</p>
  <!-- <header>
    <img alt="Vue logo"
         class="logo"
         src="./assets/logo.svg"
         width="125"
         height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main> -->
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
