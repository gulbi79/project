<template>
  <main>
    <div>
      <select>
        <option :value="city.code" :key="city.code" v-for="city in cities">{{city.title}}</option>
      </select>
    </div>
    <div>
      <table>
        <thead>
          <tr>
            <th>제품번호</th>
            <th>가격</th>
            <th>주문수량</th>
            <th>합계</th>
          </tr>
        </thead>
        <tbody>
          <tr :key="drink.id" v-for="drink in drinks">
            <td>{{drink.id}}</td>
            <td>{{drink.price}}</td>
            <td><input type="number" v-model="drink.qty"/></td>
            <td>{{drink.price * drink.qty}}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </main>
</template>
<script>
export default {
  components: {},
  data() {
    return {
      cities: [
        { title: '서울', code: '02' },
        { title: '부산', code: '051' },
        { title: '제주', code: '064' }
      ],
      drinks: [
        { id: 'a1', price: 1000, qty: 10 },
        { id: 'a2', price: 5000, qty: 20 },
        { id: 'a3', price: 7000, qty: 30 }
      ]
    }
  },
  setup() {},
  created() {},
  mounted() {},
  unmounted() {},
  methods: {}
}
</script>
