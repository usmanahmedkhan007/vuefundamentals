<template>
  <div :class="[{ active: isActive }, 'text-blue']"
       class="heading">Binding classes</div>

  <p :style="[styles, activeStyles]">Binding inline styles in vue.js</p>
</template>


<script setup>
import { ref } from 'vue'

const styles = ref({
  color: 'red',
  fontSize: '24px'
})

const activeStyles = ref({
  textTransform: 'uppercase',
  'text-decoration': 'line-through'
})
const activeColor = ref('blue')
const classes = ref({
  active: true,
  'text-blue': true
})

const isActive = ref(true)
const color = ref(true)

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
