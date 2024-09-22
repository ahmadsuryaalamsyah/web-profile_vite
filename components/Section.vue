<template>
  <div class="relative" id="about">
    <div class="bg-neutral-900 pt-[18px] sm:pt-[84px]">
      <div class="flex flex-col sm:flex-row opacity-90 w-full px-[20px] md:px-[30px] lg:px-[60px]">
        <div class="sm:w-1/2" data-aos="fade-right">
          <img class="scale-75 mx-auto" src="../assets/image/Picture.svg" alt="Picture" />
          <div class="hidden sm:flex justify-center -translate-x-10 -translate-y-14 items-center gap-4 pb-5">
            <p class="text-white text-sm font-semibold">Find Me On</p>
            <div class="flex gap-3">
              <div>
                <a href="https://www.linkedin.com/in/ahmad-surya-alam-syah-5017451b3/" target="_blank" rel="noopener noreferrer">
                  <font-awesome-icon class="grayscale hover:grayscale-0 hover:cursor-pointer hover:scale-125 duration-300 hover:text-green-500" size="xl" :icon="['fab', 'linkedin']" />
                </a>
              </div>
              <div>
                <a href="https://www.instagram.com/1_1alamsyah/" target="_blank" rel="noopener noreferrer">
                  <font-awesome-icon class="grayscale hover:grayscale-0 hover:cursor-pointer hover:scale-125 duration-300 hover:text-green-500" :icon="['fab', 'instagram']" size="xl" />
                </a>
              </div>
              <div>
                <a href="https://github.com/ahmadsuryaalamsyah" target="_blank" rel="noopener noreferrer">
                  <font-awesome-icon class="grayscale hover:grayscale-0 hover:cursor-pointer hover:scale-125 duration-300 hover:text-green-500" :icon="['fab', 'github']" size="xl" />
                </a>
              </div>
            </div>
          </div>
        </div>
        <div class="text-white flex flex-col justify-center sm:w-1/2 font-medium -translate-y-10 sm:-translate-y-0" data-aos="fade-up">
          <p class="text-2xl sm:text-3xl">Hallooo</p>
          <p class="text-2xl sm:text-3xl">Saya <span class="text-green-500 font-bold"> Ahmad Surya Alam Syah</span></p>
          <p class="text-xl">Software Developer</p>
          <div class="border-2 border-green-500 w-[80px] my-2 sm:w-[93px] lg:w-[100px]" />
          <p class="font-normal text-base">Saya Ahmad Surya Alam Syah, mahasiswi D3 Teknologi Informasi Universitas Brawijaya Malang</p>
          <div class="flex gap-3 my-4">
            <div class="bg-green-500 w-[140px] hover:scale-95 duration-300 hover:bg-green-700 text-white py-2 px-2 rounded-lg flex items-center justify-center gap-1">
              <font-awesome-icon :icon="['far', 'file']" style="color: #ffffff" />
              <a href="https://drive.google.com/file/d/1PbZoizpB7S5TqODeRs1IA2Q1ZAfmh99n/view?usp=sharing" target="_blank" rel="noopener noreferrer"> Download CV </a>
            </div>
            <button class="border-2 w-[140px] hover:scale-95 hover:bg-slate-100 hover:text-green-500 duration-300 border-green-500 py-2 px-2 rounded-lg" @click="setShowCv(true)">More</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import Aos from 'aos';
import 'aos/dist/aos.css';
import { onMounted } from 'vue';
onMounted(() => {
  Aos.init();
});

const setShowCv = (show) => {
  console.log('Show CV clicked', show);
};
</script>

<style scoped></style>
