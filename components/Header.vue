<template>
  <div class="fixed w-full z-20">
    <div class="bg-neutral-900 flex justify-between items-center py-[18px] px-[16px] lg:px-[150px]">
      <div>
        <p class="font-Poppins text-xl font-semibold text-white">Alam</p>
      </div>
      <div class="sm:hidden">
        <img @click="toggleMenu" :src="icon ? 'assets/image/close.svg' : 'assets/image/menu.svg'" :alt="icon ? 'close' : 'menu'" />
      </div>
      <div class="hidden sm:flex sm:gap-[20px] lg:gap-[40px] text-white text-base font-medium font-['DM Sans'] leading-none">
        <div class="flex flex-col justify-center items-center">
          <a class="hover:text-green-500" href="#about">About</a>
        </div>
        <div class="flex flex-col justify-center items-center">
          <a class="hover:text-green-500" href="#skill">Skill</a>
        </div>
        <div class="flex flex-col justify-center items-center">
          <a class="hover:text-green-500" href="#contact">Contact</a>
        </div>
      </div>
      <div class="hidden sm:flex w-[169px] hover:scale-95 hover:bg-green-700 duration-300 h-12 px-5 py-4 bg-green-500 rounded-lg justify-center items-center gap-2.5">
        <div class="text-white text-base font-medium font-['DM Sans'] leading-none flex gap-2">
          <a href="https://drive.google.com/file/d/1PbZoizpB7S5TqODeRs1IA2Q1ZAfmh99n/view?usp=sharing" target="_blank" rel="noopener noreferrer"> Download CV </a>
        </div>
      </div>
    </div>
    <div v-if="showMenu" class="bg-neutral-900 -mt-1 sm:hidden flex flex-col gap-[25px] py-7 justify-center text-xl items-center text-white font-semibold font-['DM Sans'] leading-none">
      <a href="#about">About</a>
      <a href="#skill">Skill</a>
      <a href="#contact">Contact</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showMenu: false,
      icon: false,
    };
  },
  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu;
      this.icon = !this.icon;
    },
  },
};
</script>

<style scoped></style>
