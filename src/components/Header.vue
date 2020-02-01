<template>
  <div>
      <div class="progress">
<div class="progress-bar" role="progressbar" aria-valuenow="70"   aria-valuemin="0" aria-valuemax="100" style="width:70%"
            :style="{width: `${percen}%`}">
         {{percen}} %
      </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Header',
    props:['quoteCount', 'maxQuote'],

    computed:{
        percen(){
            return this.quoteCount /this.maxQuote *100 
        }
    }
}
</script>

<style>

</style>