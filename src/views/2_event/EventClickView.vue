<template>
  <main>
    <button @click="increaseCounter">Add 1</button>
    <p>{{counter}}</p>
    <hr/>
    <select @change="changeCity" v-model="selectedCity">
      <option value="">== 도시선택 ==</option>
      <option :value="city.cityCode" :key="city.cityCode" v-for="city in cityList">{{city.title}}</option>
    </select>
    <select>
      <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in selectedDongList">{{dong.dongTitle}}</option>
    </select>
    <select>
      <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in dongList.filter(v => v.cityCode === selectedCity)">{{dong.dongTitle}}</option>
    </select>
  </main>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      counter: 0,
      selectedCity: '',
      cityList: [
        { cityCode: '02', title: '서울' },
        { cityCode: '031', title: '경기' },
        { cityCode: '051', title: '부산' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: '서울1동' },
        { cityCode: '02', dongCode: '2', dongTitle: '서울2동' },
        { cityCode: '02', dongCode: '3', dongTitle: '서울3동' },
        { cityCode: '031', dongCode: '1', dongTitle: '경기1동' },
        { cityCode: '031', dongCode: '2', dongTitle: '경기2동' },
        { cityCode: '051', dongCode: '1', dongTitle: '부산1동' },
        { cityCode: '051', dongCode: '2', dongTitle: '부산1동' }
      ],
      selectedDongList: []
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {
    increaseCounter() {
      this.counter += 1
    },
    changeCity() {
      this.selectedDongList = this.dongList.filter(v => v.cityCode === this.selectedCity)
    }
  }
}
</script>
