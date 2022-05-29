<template>
  <h1 @click="increase">
    {{ conut }} / {{ doubleConut }}
  </h1>
  <h1>
    {{ message }} / {{ reversedMessage }}
  </h1>
</template>

<script>
import { ref, computed } from '@vue/runtime-core'
export default {
  setup() {
    const message = ref('Hello World!')
    const reversedMessage = computed (() => {
      return message.split('').reverse().join('')
    })

    const count = ref(0)
    const doubleConut = computed(() => count * 2)
    function increase() {
      count.value += 1
    }
    return {
      message,
      reversedMessage,
      count,
      doubleConut,
      increase
    }
  }
}
</script>