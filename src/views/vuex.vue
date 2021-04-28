<template>
  <div>
    <div>vuex + count: {{ count }}</div>
    <button @click="increment">增加</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, computed } from 'vue'
import { useStore } from 'vuex'

export default defineComponent({
  setup() {
    const store = useStore()
    const count = computed(() => store.state.count)
    const increment = () => {
      store.dispatch('increment')
    }
    return {
      count,
      increment
    }
  }
})
</script>

<style scoped></style>
