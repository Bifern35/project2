<template>
    <div>
        <h1>Products List</h1>
        <HelloWorld :msg="message"></HelloWorld>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    name: 'products',
    components:{
        HelloWorld
    },
    data(){
        return{
            message:'Project2'
        }
    },
    mouted(){
        axios
        .get('https://young-beyond-66471.herokuapp.com/api/products/')
        .then(function(response){
            console.log(response.data)
        })
    }
}
</script>

