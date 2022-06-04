<template>
  <p>сверстать два инпута и привязать к ним соответствующие реактивные переменные</p>
  <p>вывести ниже блок с суммой, которая расcчитывается с помощью computed</p>

  <input type="number" v-model="a">
  <input type="number" v-model="b">
  <div>{{calculate}}</div>

  <new-component></new-component>

</template>

<script>
import NewComponent from './components/NewComponent'
export default {
  data() {
    return {
      a: '',
      b: ''
    }
  },
  computed: {
    calculate() {
      if (this.a == '') {
        return this.b;
      }
      else if (this.b == '') {
        return this.a;
      }
      return this.a + this.b;
    }
  },
  components: {NewComponent}
}
</script>

<style>

</style>
