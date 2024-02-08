<template>
  <Popover>
    <!-- Nav -->
    <Navbar />
    <!-- Header -->
    <RepairComponent />
  </Popover>
</template>

<script setup>
import { Popover } from "@headlessui/vue";
import Navbar from "./components/Navbar.vue";
import RepairComponent from "./components/Header.vue";
</script>
