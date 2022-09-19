<template>
  <main>
    <div>
      <input type="radio" id="html" value="HTML" v-model="favoriteLang"/>
      <label for="html">HTML</label>
    </div>
    <div>
      <input type="radio" id="css" value="CSS" v-model="favoriteLang"/>
      <label for="css">CSS</label>
    </div>
    <div>
      <input type="radio" id="js" value="JS" v-model="favoriteLang"/>
      <label for="js">JavaScript</label>
    </div>
    <div>선택한 지역: {{ favoriteLang }}</div>
  </main>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      favoriteLang: 'HTML'
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
