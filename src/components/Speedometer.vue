<template>
  <div class="mt-5">
    <div
      class="container-2"
      v-for="(element, index) in numb"
      :key="`id-${index}`"
    >
      <h1 class="text-center">Timing Analysis</h1>
      <!-- speedometer 1 -->
      <!--   <span class="span4">{{element.num2}}</span>
            <span class="span5">{{element.num4}}</span> -->

      <div class="circle-all">
        <div class="position-relative">
          <span class="number-speedometer1">{{ element.num1 }}</span>
          <span class="number-speedometer2">{{ element.num2 }}</span>
            <span class="number-speedometer3">{{ element.num4 }}</span>

        </div>
        <div class="cerchio"></div>
        <div>
          <svg class="circle-1">
            <circle
              class=""
              cx="105"
              cy="130"
              r="94"
              stroke="black"
              stroke-width="3"
              fill="transparent"
              stroke-linecap="round"
            />
          </svg>
        </div>
        <div>
          <svg class="circle-2">
            <circle
              cx="105"
              cy="130"
              r="94"
              stroke="black"
              stroke-width="3"
              fill="transparent"
              stroke-linecap="round"
            />
          </svg>
        </div>
        <div>
          <svg class="circle-3">
            <circle
              cx="105"
              cy="130"
              r="94"
              stroke="black"
              stroke-width="3"
              fill="transparent"
              stroke-linecap="round"
            />
          </svg>
        </div>
        <div>
          <svg class="circle-4">
            <circle
              cx="186"
              cy="84"
              r="11"
              stroke="black"
              stroke-width="3"
              fill="transparent"
              stroke-linecap="round"
            />
          </svg>
        </div>
        <div class="inside-speedometer">
          <span class="span1">{{ element.num3 }}</span>
          <div>
            <span class="span2"> Great! </span>
          </div>
        </div>
        <div class="position">
          <h1 class="text-center">Page Load</h1>
          <span>0.4s</span>
        </div>
      </div>
      <!-- speedometer 2 -->
      <div class="circle-all2">
            <div class="position-relative">
          <span class="number-speedometer4">{{ element.num1 }}</span>
          <span class="number-speedometer5">{{ element.num2 }}</span>
            <span class="number-speedometer6">{{ element.num4 }}</span>

        </div>
        <div>
          <svg class="circle-5">
            <circle
              class=""
              cx="105"
              cy="130"
              r="94"
              stroke="black"
              stroke-width="3"
              fill="transparent"
              stroke-linecap="round"
            />
          </svg>
        </div>
        <div>
          <svg class="circle-6">
            <circle
              cx="105"
              cy="130"
              r="94"
              stroke="black"
              stroke-width="3"
              fill="transparent"
              stroke-linecap="round"
            />
          </svg>
        </div>
        <div>
          <svg class="circle-7">
            <circle
              cx="105"
              cy="130"
              r="94"
              stroke="black"
              stroke-width="3"
              fill="transparent"
              stroke-linecap="round"
            />
          </svg>
        </div>
        <div>
          <svg class="circle-8">
            <circle
              cx="186"
              cy="84"
              r="11"
              stroke="black"
              stroke-width="3"
              fill="transparent"
              stroke-linecap="round"
            />
          </svg>
        </div>
       
        <div class="inside-speedometer">
          <span class="span1">{{ element.num3 }}</span>
          <div>
            <span class="span2"> Great! </span>
          </div>
        </div>
        <div class="position">
          <h1 class="text-center">First Interaction</h1>
          <span>0.9s</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Speedometer",

  data() {
    return {
      numb: [],
    };
  },
  created() {
    this.getNumberRequest();
  },

  methods: {
    getNumberRequest() {
      axios
        .get("http://myjson.dit.upm.es/api/bins/83v9")
        .then((result) => {
          console.log(result.data.response);
          this.numb = result.data.response;
        })
        .catch((err) => console.log(err));
    },
  },
};
</script>

<style lang="scss">
.container-2 {
  width: 100%;
  height: 100%;

  .text-center {
    color: rgb(125, 125, 125);
    font-weight: 600;
    font-size: 30px;
  }
  .circle-all {
    position: relative;
    display: flex;
    justify-content: center;
    .circle-1,
    .circle-2,
    .circle-3,
    .circle-4 {
      position: absolute;
      margin-left: -9px;
    }
  }
  .circle-1 {
    width: 250px;
    height: 250px;

    circle {
      fill: none;
      stroke: red;
      stroke-width: 10px;
      stroke-dasharray: 209;
      stroke-dashoffset: -206;
      position: absolute;
      z-index: 1;
    }
  }

  .circle-2 {
    width: 250px;
    height: 250px;
    circle {
      fill: none;
      stroke: rgb(229, 229, 25);
      stroke-width: 10px;
      stroke-dasharray: 400;
      stroke-dashoffset: -444;
      position: fixed;
      z-index: 2;
    }
  }
  .circle-3 {
    width: 250px;
    height: 250px;
    circle {
      fill: none;
      stroke: green;
      stroke-width: 10px;
      stroke-dasharray: 431;
      stroke-dashoffset: -524;
      z-index: 3;
    }
  }
  .circle-4 {
    width: 250px;
    height: 250px;

    circle {
      fill: none;
      stroke: green;
      stroke-width: 5px;
      z-index: 4;
    }
  }
  .inside-speedometer {
    position: absolute;
    top: 80px;

    .span1 {
      font-weight: bold;
      font-size: 30px;
    }
    .span2 {
      font-weight: 600;
      font-size: 25px;
    }
  }
  .number-speedometer1 {
    position: absolute;
    font-size: 11px;
    top: 15px;
    left: 73px;
  }
  .number-speedometer2 {
    position: absolute;
    font-size: 11px;
    top: 47px;
    left: 179px;
  }
   .number-speedometer3 {
    position: absolute;
    font-size: 11px;
    top: 171px;
    left: 196px;
  }
  .position {
    margin-top: 230px;
    h1 {
      color: rgba(181, 177, 177, 0.655);
      font-weight: bold;
      font-size: 40px;
    }
    span {
      font-weight: bold;
      font-size: 40px;
      color: rgb(102, 101, 101);
    }
  }

  .circle-all2 {
    position: relative;
    display: flex;
    justify-content: center;
    .circle-5,
    .circle-6,
    .circle-7,
    .circle-8 {
      position: absolute;
      margin-left: 38px;
    }
  }
  .circle-5 {
    width: 250px;
    height: 250px;

    circle {
      fill: none;
      stroke: red;
      stroke-width: 10px;
      stroke-dasharray: 209;
      stroke-dashoffset: -206;
      position: absolute;
    }
  }

  .circle-6 {
    width: 250px;
    height: 250px;
    circle {
      fill: none;
      stroke: rgb(229, 229, 25);
      stroke-width: 10px;
      stroke-dasharray: 400;
      stroke-dashoffset: -444;
      position: fixed;
      z-index: 8;
    }
  }
  .circle-7 {
    width: 250px;
    height: 250px;
    circle {
      fill: none;
      stroke: green;
      stroke-width: 10px;
      stroke-dasharray: 431;
      stroke-dashoffset: -524;
    }
  }
  .circle-8 {
    width: 250px;
    height: 250px;

    circle {
      fill: none;
      stroke: green;
      stroke-width: 5px;
      z-index: 4;
    }
  }
  .inside-speedometer {
    position: absolute;
    top: 80px;

    .span1 {
      font-weight: bold;
      font-size: 30px;
    }
    .span2 {
      font-weight: 600;
      font-size: 25px;
    }
  }
   .number-speedometer4 {
    position: absolute;
    font-size: 11px;
    top: 15px;
    left: 119px;
  }
  .number-speedometer5 {
    position: absolute;
    font-size: 11px;
    top: 47px;
    left: 222px;
  }
   .number-speedometer6 {
    position: absolute;
    font-size: 11px;
    top: 171px;
    left: 237px;
  }
  .position {
    margin-top: 230px;
    h1 {
      color: rgba(181, 177, 177, 0.655);
      font-weight: bold;
      font-size: 40px;
    }
    span {
      font-weight: bold;
      font-size: 40px;
      color: rgb(102, 101, 101);
    }
  }
}
</style>
