<script setup>
import { PerfectScrollbar } from "vue3-perfect-scrollbar";

defineProps({
  height: {
    type: String,
    default: "100vh",
    required: false,
  },
});
</script>

<template>
  <div>
    <perfect-scrollbar>
      <slot></slot>
    </perfect-scrollbar>
  </div>
</template>

<style src="vue3-perfect-scrollbar/dist/vue3-perfect-scrollbar.css" />

<style>
.ps {
  height: v-bind(height);
}
.ps__rail-x,
.ps__rail-y,
.ps__thumb-x,
.ps__thumb-y {
  background-color: var(--web-color-3956-ff-20, rgba(57, 86, 255, 0.2));
  width: 8px;
  height: 8px;
}
.ps__rail-x:hover > .ps__thumb-x,
.ps__rail-x:focus > .ps__thumb-x,
.ps__rail-x.ps--clicking .ps__thumb-x,
.ps__rail-y:hover > .ps__thumb-y,
.ps__rail-y:focus > .ps__thumb-y,
.ps__rail-y.ps--clicking .ps__thumb-y {
  background-color: var(--web-color-3956-ff-20, rgba(57, 86, 255, 0.2));
  width: 8px;
  height: 8px;
}
.ps:hover > .ps__rail-x,
.ps:hover > .ps__rail-y,
.ps--focus > .ps__rail-x,
.ps--focus > .ps__rail-y,
.ps--scrolling-x > .ps__rail-x,
.ps--scrolling-y > .ps__rail-y {
  opacity: 1;
}
.ps .ps__rail-x:hover,
.ps .ps__rail-y:hover,
.ps .ps__rail-x:focus,
.ps .ps__rail-y:focus,
.ps .ps__rail-x.ps--clicking,
.ps .ps__rail-y.ps--clicking {
  background-color: #ffffff00;
  opacity: 1;
}
</style>
