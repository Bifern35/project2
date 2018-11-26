<template>
    <div>
        <h1>Products List</h1>
        <HelloWorld :msg="message"></HelloWorld>
    </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
export default {
    name: 'products',
    components:{
        HelloWorld
    },
    data(){
        return{
            message:'Project2'
        }
    }
}
</script>

