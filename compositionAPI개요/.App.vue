<template>
  <h1 @click="increase">
    {{ conut }} / {{ doubleConut }}
  </h1>
  <h1>
    {{ message }} / {{ reversedMessage }}
  </h1>
</template>

<script>
export default {
  data() {
    return {
      message: 'Hello World!',
      count: 0
    }
  },
  computed: {
    doubleConut() {
      return this.count * 2
    },
    reversedMessage() {
      return this.message.split('').reverse().join('')
    }
  },
  methods: {
    increase() {
      this.count += 1
    }
  }
}
</script>