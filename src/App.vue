<template>
  <h1 v-bind="attributes">Binding attributes using v-bind</h1>

  <button v-bind:disabled="true">Submit</button>

  <!-- <p>{{ message.split(" ").reverse().join(" ") }}</p>
  <p>{{ number + 20 }}</p>
  <p>{{ true ? 'Yes' : 'No' }}</p>
  <p>{{ getRandomNumber() }}</p> -->
</template>


<script setup>
import { ref } from 'vue'

const dynamicId = ref('headingId')

const attributes = ref({
  id: 'headingId',
  class: 'content'
})
// let message = ref('hello world')
// let number = ref(10)
// function getRandomNumber()
// {
//   return Math.random()
// }

</script>

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
