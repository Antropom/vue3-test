<template>
  <h1>Hello test Vue 3</h1>
  <BaseInput v-model:modelValue="myInput" />
  <h2>{{ myInput }}</h2>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import BaseInput from './components/BaseInput.vue'

export default defineComponent({
  name: 'App',
  components: {
    BaseInput,
  },
  data() {
    return {
      myInput: '',
    }
  },
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
