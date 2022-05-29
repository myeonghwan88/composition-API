<template>
  <div @click="increase">
    {{ count }}
  </div>
</template>

<script>
import { ref } from 'vue'
// 반응성을 가지기 위해 ref 함수를 vue에서 가져온다

export default {
  // data() {
  //   return {
  //     count: 0
  //   }
  // },
  // methods: {
  //   increase() {
  //     this.count += 1
  //   }
  // },
  setup() {
    let count = ref(0)
    function increase() {
      count.value += 1
    }

    return {
      count,
      increase
    }
  }
}
</script>