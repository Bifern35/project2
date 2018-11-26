<template>
    <div>
        <h1>Products List</h1>
        <b-table striped hover :items="products" :fields="fields"></b-table>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    name: 'products',
    data(){
        return{
            message:'Project2',
            products: [],
            fields:[{
                key:'id',
                sortable : true
            },{
                key:'title',
                sortable : true
            },{
                key:'price',
                sortable : true,
                variant: 'danger'
            }]        
        }
    },
    mounted(){
        var instance = this
        axios
        .get('https://young-beyond-66471.herokuapp.com/api/products/')
        .then(function(response){
            console.log(response.data)
            instance.products = response.data.data
        })
    }
}
</script>

