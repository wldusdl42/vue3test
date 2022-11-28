<script setup>
import { reactive } from 'vue'

const list = reactive([])
const onClick = () => {
  list = [...list , 'a']
}
</script>

<template>
  <h1> List: {{ list.join(', ')  }} </h1>
  <button @click='onClick'>
    add
  </button>
</template>