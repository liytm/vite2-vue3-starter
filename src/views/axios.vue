<template>
  <div>axios + count: {{ count }}</div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup() {
    const count = ref(0)
    return {
      count
    }
  }
})
</script>

<style scoped></style>
