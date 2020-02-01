<template>
  <div class="row">
        <form >
            <div class="col-md-6 col-xs-12 form-group" >
                <label>Qutoe</label>
                <textarea class="form-control rows-3" v-model="msg" > </textarea>
            </div>
            <div class="col-md-6 col-xs-12 form-group" >
                
               <button class="btn btn-primary" @click.prevent="addQuote">Add</button>
            </div>

        </form>
  </div>
</template>

<script>
export default {
    name: 'NewQuote',
    data(){
        return{
            msg:''
        }

    },
    methods:{
        addQuote(){
            
                this.$emit('submit', this.msg)
                this.msg=''
        }
    }
}
</script>

<style>

</style>