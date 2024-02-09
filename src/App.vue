<template>
  <Popover>
    <!-- Nav -->
    <Navbar />
  </Popover>
  <!-- Header -->
  <RepairComponent />
  <!-- Multistepform -->
  <MultiStepForm />
</template>

<script setup>
import { Popover } from "@headlessui/vue";
import Navbar from "./components/Navbar.vue";
import RepairComponent from "./components/Header.vue";
import MultiStepForm from "./components/MultiStepForm.vue";
</script>
