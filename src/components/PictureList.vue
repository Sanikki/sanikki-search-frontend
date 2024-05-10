<template>
  原神启动
  <nav />
  <img class="madoka" :src="madoka" />
</template>

<script setup lang="ts">
import madoka from "../assets/madoka.png";
</script>

<style scoped>
.madoka {
  height: 400px;
}
</style>
