<template>
  <input type="number" v-model="a">
  <input type="number" v-model="b">
  <div v-if="calculate !== 0">{{calculate}}</div>
</template>

<script>

import {ref, computed} from 'vue'

export default {
    setup() {
        const a = ref(null)
        const b = ref(null)

        const calculate = computed(() => {
            return a.value + b.value
        }) 

        return {a, b, calculate}
    }
}
</script>

<style>

</style>