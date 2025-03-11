<template>

  <div class="min-h-screen flex flex-col items-center justify-start py-10 px-4 bg-black text-teal-100">

    <div class="w-[1024px] rounded-lg p-8 bg-gradient-to-br from-emerald-950 to-indigo-950 shadow-lg">

      <div class="text-center">
        <h1 class="text-[60px] font-bold">
          <span class="text-teal-100">Pozdrav, ja sam</span> <span class="text-cyan-400">Iva Batur</span>
        </h1>
        <div class="w-full h-[2px] bg-teal-100/75 mt-2 "></div> 
      </div>

  
      <h2 class="text-[24px] text-teal-100/75 mt-4">Moji omiljeni filmovi:</h2>

  
      <div class="mt-6 grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
        <div v-for="film in filmovi" :key="film.naslov" class="flex flex-col items-center">
          <div class="w-[320px] h-[480px] rounded-[6px] overflow-hidden shadow-lg bg-gray-200 dark:bg-gray-700">
            <img :src="film.slika" :alt="film.naslov" class="w-full h-full object-cover">
          </div>
          <div class="text-[24px]  text-white text-center mt-2">{{ film.naslov }}</div> 
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      filmovi: [
        { naslov: "Čudo u ćeliji br. 7", slika: "/Snimka zaslona 2025-03-10 123856.png" },
        { naslov: "6888. bojna", slika: "/Snimka zaslona 2025-03-10 123947.png" },
        { naslov: "Milijunaš s ulice", slika: "/Snimka zaslona 2025-03-10 185359.png" }
      ]
    };
  }
};
</script>
