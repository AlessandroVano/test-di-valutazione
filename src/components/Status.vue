<template>
   <div>
       <div v-for="(element, index) in stat" :key="`id-${index}`">
      <div>
        <div class="mt-5 fs-1">{{ element.status }}</div>
        <span>{{ element.errors }}</span>
      </div>
      
      
    </div>

   </div>
</template>

<script>
import axios from "axios";
export default {
    name: 'Status',


    data() {
        return {
            stat: [],
        };
    },

    created() {
    this.getCreateHttprequest();
  },
  methods: {
      getCreateHttprequest() {
         axios
           .get("http://myjson.dit.upm.es/api/bins/2ohx")
           .then((result) => {
            /*  console.log(result.data.response); */
             this.stat = result.data.response;
           })
           .catch((err) => console.log(err));
       },

  }
  
}



</script>

<style>

</style>