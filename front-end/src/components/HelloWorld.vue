<template>
  <div >
    <form  method="post">
        <input v-model="name">
        <input v-model="email">
        <input v-model="bar_code">
        <button></button>
    </form>
    <div class="line">
      <div class="column">
        <Card  v-bind="products" />
        <Card v-bind="products"/>
        <Card v-bind="products"/> 
      </div>
    </div>
    {{ products }}
  </div>
</template>

<script lang="ts">
import axios  from 'axios';
import { defineComponent } from 'vue';
import Card from "./Card.vue";

export default defineComponent({
  name: 'HelloWorld',
  
  data() {
    return {
      id:'',
      name: '',
      email:'',
      bar_code:'',
      products: []
    }
    
  },
  components:{
    Card
  },
  methods:{

  },
  mounted () {
    axios
      .get('http://localhost:3000/product')
      .then(response => (this.products = response.data[0]))
      .catch((error) => {
        console.log(error);
      });
      console.log(this.products)
  }
  
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.column{
  display: flex;
  justify-content: center;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
