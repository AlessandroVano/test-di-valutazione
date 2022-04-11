<template>
  <section class="container flex-column">
    <div class="flex-grow-1">
    <div class="row justify-content-center  ">
      <!-- card 1 -->
      <div class=" card col-11 col-md-3 my-1 ">
        <div v-for="(element, index) in stat" :key="`id-${index}`">
          <div class="d-flex mb-2">
            <h4 class="card-title mt-2">{{ element.title1 }}</h4>
          </div>
          <div>
          <!-- blocco 1 -->
          <div class="bg">
            <div class="d-flex px-2  ">
              <h5>
                {{ element.title2 }}
              </h5>
            </div>
            <div class="d-flex px-2 text">
              {{ element.span1 }}
            </div>
          </div>
          <!-- blocco 2 -->
          <div class="bg my-1">
            <div class="d-flex px-2">
              <h5>
                {{ element.title3 }}
              </h5>
            </div>
            <div class="d-flex px-2 text">
              {{ element.span2 }}
            </div>
          </div>
          <!-- blocco 3 -->
          <div class="bg">
            <div class="d-flex px-2">
              <h5>
                {{ element.title4 }}
              </h5>
            </div>
            <div class="d-flex px-2 text">
              {{ element.span3 }}
            </div>
          </div>
            
          </div>
        </div>
      </div>
      <!-- card 2 -->
      <div class=" card card-style mx-2  col-11 col-md-3 my-1 ">
        <div v-for="(element, index) in stat" :key="`id-${index}`">
          <div class="d-flex">
            <h3 class="card-title">{{ element.title5 }}</h3>
          </div>
          <div class="d-flex bg-2  px-2">
            {{ element.span4 }}
          </div>
          <div class="d-flex bg-2 m px-2">
            {{ element.span5 }}
          </div>
          <div class="d-flex bg-2 px-2">
            {{ element.span6 }}
          </div>
        </div>
      </div>
      <!-- card 3 -->
   
        <div class="card card-style mx-2 col-11 col-md-3 my-1">
        <div v-for="(element, index) in stat" :key="`id-${index}`">
          <div class="d-flex">
            <h3 class="card-title">{{ element.title5 }}</h3>
          </div>
          <div class="d-flex bg-2  px-2">
            {{ element.span4 }}
          </div>
          <div class="d-flex bg-2 m px-2">
            {{ element.span5 }}
          </div>
          <div class="d-flex bg-2 px-2">
            {{ element.span6 }}
          </div>
        </div>
      </div>

      <div class="text-center mt-5 mb-5">
        <h1> SHARE</h1>
        <span>httprequest.com/1a54da6848864</span>
      </div>
    </div>

    </div>
  </section>
</template>

<script>
import axios from "axios";
export default {
  name: "Information",

  data() {
    return {
      stat: [],
      /*  response1: "",
      response2: "", */
    };
  },

  created() {
    this.getResultrequest();
  },
  methods: {
    getResultrequest() {
      axios
        .get("http://myjson.dit.upm.es/api/bins/f9i9")
        .then((result) => {
          console.log(result.data.response);
          this.stat = result.data.response;
          /*  this.response1 = result.data.response[0].title1;
          this.response2 = result.data.response[1].title3; */
         /*  console.log(this.response1);
          console.log(this.stat[1]); */
        })
        .catch((err) => console.log(err));
    },
  },
};
</script>

<style lang="scss">
.card {
  background-color: #ececec !important;
  padding-right: 0 !important;
  padding-left: 0 !important ;
  max-height: 200px !important;
  .card-title {
    font-size: 0.9rem;
    padding-left: 0.6rem;
  }
  .bg {
    background-color: rgb(211, 208, 208);
    h5{
      font-size: 1.1rem ;
       font-weight: bold;
       color: rgba(8, 8, 8, 0.723)
    }
    .text{
      margin-top: -13px;
    }
  }
  /* Card 2 */
}
  .card-style{
    background-color: white !important;
   .m{
     margin-top: 1px;
     margin-bottom: 1px;
   }
     .bg-2{
        background-color: #ececec;
     }
  }

  .text-center{
    h1{
      font-size: 25px;
      font-weight: 600;
    }
    span{
      background-color: #ececec;
      padding: 5px 15px 5px 15px;
      border-radius: 20px ;
    
    }
  }
</style>
