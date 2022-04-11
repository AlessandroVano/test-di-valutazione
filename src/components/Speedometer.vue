<template>
  <div class="mt-5">
    <div class="container-2">
      <h1 class="text-center">Timing Analysis</h1>
      <!-- speedometer 1 -->
      <div class="circle-all">
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
          <!--     <svg class="circle-4">
              <circle
                cx="130"
                cy="130"
                r="100"
                stroke="black"
                stroke-width="3"
                fill="transparent"
                stroke-linecap="round"
              />
            </svg> -->
        </div>
        <div class="inside-speedometer">
          <span class="span1">720</span>
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
          <!--     <svg class="circle-4">
              <circle
                cx="130"
                cy="130"
                r="100"
                stroke="black"
                stroke-width="3"
                fill="transparent"
                stroke-linecap="round"
              />
            </svg> -->
        </div>
        <div class="inside-speedometer">
          <span class="span1">720</span>
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
export default {
  name: "Speedometer",

  /* mounted() {
    let progressCircle = document.querySelector(".circle-2");
    let radius = progressCircle.r.baseVal.value;

    let circumferenze = radius * 2 * Math.PI;
    progressCircle.style.strokeDasharray = circumferenze;

    setProgress(50);

    function setProgress(percent) {
     progressCircle.style.strokeDashoffset = circumferenze;
    }
  } */
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
      z-index: 8;
    }
  }
  .circle-3 {
    width: 250px;
    height: 250px;
    circle {
      fill: none;
      stroke: green;
      stroke-width: 10px;
      stroke-dasharray: 587;
      stroke-dashoffset: -667;
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
    .circle-7 {
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
      stroke-dasharray: 587;
      stroke-dashoffset: -667;
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
