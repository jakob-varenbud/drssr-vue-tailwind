<template>
  <div class="p-3 md:p-8">
    <Popover>
      <!-- Nav -->
      <Navbar />
      <!-- Header -->
      <RepairComponent />
    </Popover>
  </div>
</template>

<script setup>
import { Popover } from "@headlessui/vue";
import Navbar from "./components/Navbar.vue";
import RepairComponent from "./components/Header.vue";
</script>
