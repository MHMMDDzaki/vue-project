<template>
<!-- Data Binding -->
  <!-- <a :href="url">Go to MFIKRI</a> -->
<!-- Two Way Data Binding -->
<!-- <input type="text" v-model="nama">
  {{ nama }} -->
<!-- Conditional & loops -->
<div v-if="product.length">
  <ul>
    <li v-for="item in product" :key="item.id">
      {{ item.title }} - {{ item.price }}
    </li>
  </ul>
</div>
<div v-else>
  <p>No Data Found</p>
</div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      // url: "https://mfikri.com"
      // nama: "Abrar",
      product:[
        {id: 1, title:"Product 1", price:3000},
        {id: 1, title:"Product 2", price:5000},
        {id: 1, title:"Product 3", price:2000},
        {id: 1, title:"Product 4", price:10000},
        {id: 1, title:"Product 5", price:7000}
      ]
    };
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
