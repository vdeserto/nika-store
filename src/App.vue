<script setup lang="ts">
import {  RouterView } from "vue-router";
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
 
  <Navbar />

  <RouterView class="main-app" />

  <Footer />
</template>

<style>
@import "@/assets/base.css";

.main-app {
  min-height: 100vh;
}
</style>
