<template>
  <div id="app" class="container-fluid">
    <div class="row">
      <div class="page-1" v-show="view === false">
        <!-- <div
          id="page1"
          ontouchstart="p1handleTouchStart(event)"
          ontouchmove="p1handleTouchMove(event)"
          ontouchend="p1handleTouchEnd(event)"
        >
        </div> -->
        <button @click="view = true">click me</button>
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
        <button @click="view = false">click me</button>
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
         /*  p1 : document.getElementById("page1"),
          p2 = document.getElementById("page2"),
          startingX = null */
        }
    },

 /*  mounted() {
    let p1 = document.getElementById("page1");
    let p2 = document.getElementById("page2");
    let startingX;

    function p1handleTouchStart(evt) {
      startingX = evt.touches[0].clientX;
    }
    function p2handleTouchMove(evt) {
      let touch = evt.touches[0];
      let change = startingX - touch.clientX;
      if (change < 0) {
        return;
      }
      p1.style.left = "-" + change + "px";
      p2.style.display = "block";
      p2.style.left = screen.width - change + "px";
      evt.preventDefault();
    }
    function p2handleTouchEnd(evt) {
      var change = startingX - evt.changedTouches[0].clientX;
      var threshold = screen.width / 3;
      if (change < threshold) {
        p1.style.left = 0;
        p2.style.left = "100%";
        p2.style.display = "none";
      } else {
        p1.style.transition = "all .3s";
        p2.style.transition = "all .3s";
        p1.style.left = "-100%";
        p2.style.left = "0";
        p2.style.display = "block";
      }
    }
  }, */
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
  }
  .swipe { 
    position: absolute;
    overflow: hidden;
    top: 0;
    left: 0;
    width: 100vw;
    height: 0; 
   /*  background-color:  rgba(0, 0, 0, 0.496); */
    transition: all .3s ease-in-out;
    &.view {
      height: 110vh;
    }
  }
}
</style>
