<template>
  <div>
    <h1>Product List</h1>
    <b-table striped hover :items="products" :fields="fields" :per-page="pageSize" :current-page="pageIndex"></b-table>
    <b-pagination align="center" size="lg" :total-rows="products" v-model="pageIndex" :per-page="pageSize">
    </b-pagination>
  </div>
</template>

<script>
import axios from 'axios'
export default {
    name: 'product',
  components: {
    
  },
  data(){
      return{
          message: 'Project22'
      }
  },
   data(){
      return{
          message: 'Project2',
          products: [],
          pageSize: 10,
          pageIndex:1,
           fields: [ 
               {
                   key:'product_id',
                   sortable :true
               },
               {
                    key:'title',
                   sortable :true
               },
               {
                    key:'price',
                   sortable :true,
                   variant: 'danger'
               },
               ],
      }
  },
  mounted(){
      var instance = this
      axios
      .get('https://infinite-ravine-97956.herokuapp.com/api/products')
      .then(function(response){
console.log(response.data)
instance.products =response.data.data
      })
  }
}
</script>

