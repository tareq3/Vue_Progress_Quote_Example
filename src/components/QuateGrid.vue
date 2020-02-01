<template>
  <div class="row">
        <Quate  v-for="quate in quates" :key="quate" @click.native="deleteQ"> 
            <p>{{quate}}</p>
        </Quate>
  </div>
</template>

<script>
import Quate from'./Quate'
export default {
        name: 'QuateGrid',
        props:['quates'],
        components:{
            Quate
        },
        methods:{
            deleteQ(){
                console.log('deleteQ')
            }
        }
}
</script>

<style>

</style>