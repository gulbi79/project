<template>
  <main>
    <input type="text" v-model="userId"/>
    <button @click="myFunction">클릭</button>
    <button @click="changeData">클릭</button>
    <br/>
    <input type="text" v-model="num1"/>+
    <input type="text" v-model="num2"/>=
    <span>{{num1 + num2}}</span>
    <br/>
    <input type="text" v-model.number="num3"/>+
    <input type="text" v-model.number="num4"/>=
    <span>{{num3 + num4}}</span>
  </main>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'kwangsung.kim',
      num1: 0,
      num2: 0,
      num3: 0,
      num4: 0
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    myFunction() {
      console.log('userId', this.userId)
    },
    changeData() {
      this.userId = '지유'
    }
  }
}
</script>
