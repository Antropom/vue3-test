<template>
  <h1>Hello test Vue 3</h1>
  <BaseInput v-model:modelValue="form.myInput" />
  <SalutationName
    v-model:salutation="form.salutation"
    v-model:name="form.name"
  />
  <h2>{{ form.myInput }}</h2>
  <h2>Hello {{ form.salutation }} {{ form.name }}</h2>
</template>

<script lang="ts">
import { defineComponent, reactive } from 'vue'
import BaseInput from './components/BaseInput.vue'
import SalutationName from './components/SalutationName.vue'

export default defineComponent({
  name: 'App',
  components: {
    BaseInput,
    SalutationName,
  },
  setup() {
    const form = reactive({
      myInput: '',
      salutation: '',
      name: '',
    })

    return {
      form,
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
