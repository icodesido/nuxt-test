<template>
  <div class="fade-test">
    <button v-on:click="show = !show">
      Toggle transition
    </button>

    Duration: 
    <input v-model="duration" type="range" min="100" max="3000">
    {{duration}}ms

    <fade-transition mode="out-in" :duration="durationNumber">
    <div key="blue" v-if="show" class="box"></div>
    <div key="red" v-else class="red-box"></div>
  </fade-transition>
  </div>
</template>

<script>
import FadeTransition from "./FadeTransition.vue";
export default {
  components: {
    FadeTransition
  },
  data() {
    return {
      show: true,
      duration: 300
    };
  },
  computed: {
    durationNumber() {
      return parseInt(this.duration);
    }
  }  
};
</script>
<style lang="scss">
$r-al: right;

.fade-test {
  float: $r-al;

  & button {
    float: $r-al;
  }
}
.box {
  width: 200px;
  height: 200px;
  margin-top: 20px;
  background-color: rgb(108, 141, 213);
  box-shadow: rgba(108, 141, 213, 0.5) 0px 6px 20px;
  border-radius: 10px;
}
.red-box {
  @extend .box;
  background-color: rgb(251, 17, 116);
  box-shadow: rgba(251, 17, 116, 0.5) 0px 6px 20px;
}
</style>