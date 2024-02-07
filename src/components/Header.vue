<template>
  <div
    class="flex flex-col md:flex-row md:justify-between bg-white p-6 font-dm-sans"
  >
    <div>
      <div class="text-green-500 text-sm">★★★★☆ Trustpilot</div>
      <h2 class="text-2xl font-bold text-gray-800 my-2">DRS Smart Repair</h2>
      <p class="text-lg text-gray-700">Kleine Schäden schnell beheben.</p>
      <ul class="my-4">
        <li class="flex items-center">
          <svg
            class="h-4 w-4 text-green-500 mr-2"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M5 13l4 4L19 7"
            />
          </svg>
          Für Parkschäden, Dellen, Kratzer, Steinschläge und Innenraum
        </li>
        <li class="flex items-center">
          <svg
            class="h-4 w-4 text-green-500 mr-2"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M5 13l4 4L19 7"
            />
          </svg>
          Kostengünstig und schnell
        </li>
        <li class="flex items-center">
          <svg
            class="h-4 w-4 text-green-500 mr-2"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M5 13l4 4L19 7"
            />
          </svg>
          Einfach Foto schicken und zum Festpreis reparieren lassen
        </li>
      </ul>
      <a href="#" class="inline-block bg-drs-red text-white py-2 px-4 rounded"
        >Zur Anfrage in 3 Schritten</a
      >
    </div>
  </div>

  <!-- Bild und Kontakt-Button für Mobile -->
  <div class="relative mt-4 md:mt-0">
    <img
      class="w-full rounded-lg shadow-lg"
      src="https://uploads-ssl.webflow.com/642d8b6e384132be9f422e44/659e9db5fb95e3e30645b49f_drs-smartrepair.de%20Hero%20image_4%20(1).png"
      alt="Auto in Reparaturwerkstatt"
    />
    <button
      class="absolute bottom-0 right-0 mb-4 mr-4 bg-green-500 text-white p-2 rounded-full shadow-lg"
    >
      <img
        class="h-6 w-6"
        src="https://uploads-ssl.webflow.com/642d8b6e384132be9f422e44/6436781f71e7a80cd9c2abdd_WhatsApp.svg"
        alt="WhatsApp Icon"
      />
    </button>
  </div>
</template>

<script>
export default {
  name: "RepairComponent",
  // Hier können Sie Daten, Methoden und andere Optionen für die Komponente definieren.
};
</script>
