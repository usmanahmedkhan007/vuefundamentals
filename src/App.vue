<template>
  <p>{{ rawHtml }}</p>
  <p v-html="rawHtml"></p>

  <div :class="[{ active: isActive }, 'text-blue']"
       class="heading">Binding classes</div>
</template>


<script setup>
import { ref } from 'vue'

const classes = ref({
  active: true,
  'text-blue': true
})

const isActive = ref(true)
const color = ref(true)
const rawHtml = ref('<span style="color : red;">This should be red</span>')

</script>

<style scoped>
.active {
  font-size: 2.4rem;
  /* color: red; */
}

.text-blue {
  color: blue;
}
</style>
