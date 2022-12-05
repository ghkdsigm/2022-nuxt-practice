<template>
  <div>
    홈
    <p>{{ product }}</p>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'MainPage',
  async asyncData() {
    const response = await axios.get('http://localhost:3000/products')
    // console.log(response)
    const product = response.data
    return { product }
  },
  // async created() {
  //   const response = await axios.get('http://localhost:3000/products')
  //   console.log(response)
  //   return { response }
  // },
}
</script>

<style></style>
