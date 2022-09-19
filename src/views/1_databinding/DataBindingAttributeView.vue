<template>
  <main>
    <div>
      <input type="text" v-bind:value="userId" readonly/>
      <input type="text" :value="userId" readonly/>
      <br/>
      <img :src="imgSrc" style="width:100px; height: auto;"/>
      <br/>
      <input type="search" v-model="txt1" />
      <button :disabled="txt1 === ''">조회</button>
    </div>
  </main>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      userId: 'sung',
      imgSrc: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/2367px-Vue.js_Logo_2.svg.png',
      txt1: ''
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
