<template>
  <div>
    <!-- Render the current step -->
    <div v-if="step === 1">
      <div class="grid grid-cols-2 mb-4">
        <!--for each lopp like v-for -->
        <div
          class="flex gap-2"
          v-for="checkbox in checkboxData"
          :key="checkbox.id"
        >
          <input
            type="checkbox"
            :id="checkbox.id"
            :value="checkbox.id"
            :checked="selectedCheckboxes.includes(checkbox.id)"
            @change="handleCheckboxChange(checkbox.id)"
          />
          <!-- v-bind : and {{  }} for rendering dynamic value like checbockbox data-->
          <label :for="checkbox.id">{{ checkbox.label }}</label>
        </div>
      </div>
      <button :disabled="!isStepOneComplete" @click="step++">Next</button>
    </div>

    <div v-if="step === 2">
      <input
        type="text"
        name="preName"
        v-model="formData.preName"
        placeholder="Pre Name"
      />
      <input
        type="text"
        name="name"
        v-model="formData.name"
        placeholder="Name"
      />
      <input
        type="email"
        name="email"
        v-model="formData.email"
        placeholder="Email"
      />
      <input
        type="tel"
        name="phone"
        v-model="formData.phone"
        placeholder="Phone"
      />
      <textarea
        name="message"
        v-model="formData.message"
        placeholder="Your message"
      />
      <button :disabled="!isStepTwoComplete" @click="submitForm">Submit</button>
    </div>
  </div>
</template>

<script>
import { ref, computed } from "vue";

export default {
  setup() {
    const step = ref(1);
    const selectedCheckboxes = ref([]);
    const formData = ref({
      preName: "",
      name: "",
      email: "",
      phone: "",
      message: "",
    });

    const checkboxData = [
      { id: 1, label: "Delle" },
      { id: 2, label: "Kratzer" },
      { id: 3, label: "Innenraum" },
      { id: 4, label: "Felge" },
      { id: 5, label: "Hagelschaden" },
    ];

    const handleCheckboxChange = (checkboxId) => {
      const index = selectedCheckboxes.value.indexOf(checkboxId);
      if (index !== -1) {
        selectedCheckboxes.value.splice(index, 1);
      } else {
        selectedCheckboxes.value.push(checkboxId);
      }
    };

    // Berechnete Eigenschaft, die prüft, ob Bedingungen für Schritt 1 erfüllt sind
    const isStepOneComplete = computed(() => {
      return selectedCheckboxes.value.length > 0;
    });

    // Für Schritt 2, prüfen Sie, ob alle erforderlichen Felder ausgefüllt sind
    const isStepTwoComplete = computed(() => {
      return (
        formData.value.preName &&
        formData.value.name &&
        formData.value.email &&
        formData.value.phone
      );
    });

    const submitForm = () => {
      console.log("Formular Daten:", formData.value);
      // Hier könnten Sie weitere Aktionen durchführen, wie z.B. die Daten an einen Server senden
    };

    return {
      step,
      selectedCheckboxes,
      formData,
      checkboxData,
      isStepOneComplete,
      isStepTwoComplete,
      handleCheckboxChange,
      submitForm,
    };
  },
};
</script>
