<template>
  <main>
    <select v-model="selectCity">
      <option value=""></option>
      <option value="02">서울</option>
      <option value="031">경기</option>
      <option value="051">부산</option>
    </select>
  </main>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      selectCity: '051'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
