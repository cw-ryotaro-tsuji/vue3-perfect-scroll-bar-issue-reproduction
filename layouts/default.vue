<script setup>
import PerfectScrollbar from "@/components/PerfectScrollbar.vue";
</script>

<template>
  <PerfectScrollbar>
    <slot></slot>
  </PerfectScrollbar>
</template>

<style>
html {
  background-color: grey;
  overflow: hidden;
}
</style>
