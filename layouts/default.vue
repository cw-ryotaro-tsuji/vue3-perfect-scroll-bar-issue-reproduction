<template>
  <NuxtScrollbar class="box">
    <slot></slot>
  </NuxtScrollbar>
</template>

<style>
html {
  background-color: grey;
  overflow: hidden;
}
.box {
  height: 100vh;
}
</style>
