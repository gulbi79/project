<template>
  <main>
    <div :class="{ 'error': hasError, active: isActive }">클래스 바인딩</div>
    <button @click="fn_error">Error</button>
    <button @click="fn_active">Active</button>
    <br/>
    <div :class="class2">클래스 바인딩2</div>
  </main>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      isActive: false,
      hasError: false,
      class2: ['active', 'error']
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    fn_error() {
      this.hasError = true
    },
    fn_active() {
      this.isActive = true
    }
  }
}
</script>
<style scoped>
.active {
background-color: greenyellow;
font-weight: bold;
}
.error {
  color: red;
}
</style>
