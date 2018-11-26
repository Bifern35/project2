<template>
    <div>
        <h1>Users List</h1>
        <HelloWorld :msg="message"></HelloWorld>
    </div>
</template>

<script>
import HelloWorld from '@/components/HelloWorld.vue'
export default {
    name: 'users',
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

