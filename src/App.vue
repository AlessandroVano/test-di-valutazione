<template>
  <div id="app" class="container-fluid">
    <div class="row">
      <div class="page-1" :class="{view : view == false}" >
      
      
        <button class="btn"  @click="view = true">Swipe</button>
          <Status />

          <Input />

          <Information />
      </div>

      <div class="swipe" :class="{view : view == true}">
      <!--   <div
          id="page2"
          ontouchstart="p2handleTouchStart(event)"
          ontouchmove="p2handleTouchMove(event)"
          ontouchend="p2handleTouchEnd(event)"
        >
        </div> -->
        <button class="btn" @click="view = false">Swipe</button>
          <Speedometer />
      </div>
    </div>
  </div>
</template>

<script>
import Status from "@/components/Status.vue";
import Input from "@/components/Input.vue";
import Information from "@/components/Information.vue";
import Speedometer from "@/components/Speedometer.vue";

export default {
  name: "App",
  components: {
    Status,
    Input,
    Information,
    Speedometer,
  },
   data() {
        return {
          view : false,
        }
    },

};

</script>

<style lang="scss">
#app {
  
  text-align: center;
  .page-1 {
    position: absolute;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
  /*   opacity: 100%; */
    transition: all 1s ease-in-out;
     
    &.view{
       height: 0;
    }
  }
  .swipe { 
    position: absolute;
    overflow: hidden;
    top: 0;
    left: 0;
    width: 100vw;
    height: 0; 
    transition: all 1s ease-in-out;
       background-color: white;
  
     &.view {
      height: 110vh;
    } 
  }
}
</style>
