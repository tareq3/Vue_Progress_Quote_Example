<template>
  <div class="col-sm-4">
      <div class="panel panel-default">
          <div class="panel-body  ">
        <slot>  </slot>
          </div>
        </div>
  </div>
</template>

<script>
export default {
        name: 'quate',
       
}
</script>

<style>
.panel-body{
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;

}

.panel-body:hover{
    background-color: aquamarine; 
}


</style>