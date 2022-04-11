<template>
<div class="mt-3 d-flex  justify-content-center  col-12 mb-5 ">
  <div>
  <select class="form-select col-1 mr" >
  <option value="1">GET</option>
  <option value="2">POST</option>
  <option value="3">DELETE</option>
</select>

  </div>
<input type="text" class="mx-1 input_class">
<button class="btn btn-primary ">SEND</button>

</div>
</template>

<script>

export default {
name: 'Input'
}
</script>

<style lang="scss">

.bordr {
   
    padding-top: 12px;
    padding-left: 1px ;
    padding-bottom: 10px;
    background: rgba(128, 128, 128, 0.529);
    border-radius: 12px;
  .input_class{
      border: none;
        background: transparent;
      :focus-visible{
        
          box-shadow: transparent !important;
      }
  }
  .btn {
    padding-left: 30px;
    padding-right: 30px ;
  }
}

</style>