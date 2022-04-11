<template>
  <div id="app" class="container-fluid">
    <div class="row">
      <Status />

      <Input />

      <Information />
      <Speedometer />
    </div>
  </div>
</template>

<script>
import Status from "@/components/Status.vue";
import Input from "@/components/Input.vue";
import Information  from "@/components/Information.vue";
import Speedometer from "@/components/Speedometer.vue";

export default {
  name: "App",
  components: {
    Status,
    Input,
    Information,
    Speedometer
    
  },

  /*  data() {
    return {
      request: [],
    };
  },

  created() {
    this.getCreateHttprequest();
  },
  methods: {
    getCreateHttprequest() {
      axios
        .get("http://myjson.dit.upm.es/api/bins/8vhp")
        .then((result) => {
          console.log(result.data.response);
          this.request = result.data.response;
        })
        .catch((err) => console.log(err));
    },
  }, */
};
</script>

<style lang="scss">
#app {
  text-align: center;
}
</style>
